# MissionBehaviour

Mission Behaviours are used to control the [Mission](../mission.md). This can be anything from spawning [Agents](../agent.md) to adding boundaries for the Mission. A mission can have any amount of mission behaviours.

[MissionLogic](missionlogic.md) and [MissionViews](missionview.md) are both types of MissionBehaviours \(they inherit MissionBehaviour\).

## Properties

* `BehaviourType` - Type of the mission behaviour. Currently can be Logic or Other. MissionLogic instances have Logic as set. For other mission behaviours, use of Other is recommended.
* `DebugInput` - IInputContext instance for debugging. Note that released builds may not have a working instance.
* `Mission` - [Mission](../mission.md) of this mission behaviour. If you add same mission behaviour instance to multiple missions, this property will hold the last one. Note that using same mission behaviour instance with multiple missions is not recommended unless you know what you are doing.

## Mission Callbacks

* `OnAfterMissionCreated()` - Called right after the mission is created on C\# side. Call of this callback will be the first method call of the mission beaviour. However, mission behaviours added after the mission is created won't have this callback called.
* `OnBehaviourInitialize()` - Called right after the mission is fully created. This is the recommended callback for initialization. If a mission behaviour \(including official ones\) is added after the mission creation, this callback should be called manually.
* `OnCreated()` - Called whenever a mission behaviour is added to a mission.
* `EarlyStart()` - Called at the mission start, right before `AfterStart` callback.
* `AfterStart()` - Called at the mission start.
* `OnRenderingStarted()` - Called when rendering of the scene is started.
* `OnPreMissionTick(float)` - Called at the start of tick on the engine side.
  * `float` - Time passed since last tick.
* `OnPreDisplayMissionTick(float)` - Called at the start of tick mission tick. Note that this is called before agents and teams are ticked and also before `OnMissionTick`.
  * `float` - Time passed since last tick.
* `OnMissionTick(float)` - Called once every frame.
  * `float` - Time passed since last tick.
* `OnMissionActivate()` - Called when a deactivated mission is activated.
* `OnMissionDeactivate()` - Callend when a mission is deactivated.
* `OnMissionModeChange(MissionMode, bool)` - Called when mode of a mission is changed.
  * `MissionMode` - Old mode.
  * `bool` - True if it is the start of mission.
* `OnClearScene()` - Called when the scene is being cleared. Note that this is called after after `OnRemove` and `OnDelete` called for all agents in the scene. This is the recommend callback for resetting mission behaviour when mission is reset.
* `HandleOnCloseMission()` - Called when a mission is about to end. It is not recommend to override and use this callback. Prefer other callbacks like `OnEndMission` for end of the mission tasks.
* `OnEndMission()` - Called when mission is ending. This is the recommend callback for end of the mission tasks. It is also recommended to unregister events in this callback if any registered.
* `OnRemoveBehaviour()` - Called when a mission behaviour is removed from a mission. Note that mission behaviours are removed at the end of a mission, after resources are cleared and after `OnEndMission` callback.

## Agent Callbacks

* `OnAgentCreated(Agent)` - Called after an agent created on the engine side. Called before OnAgentBuild. This is the recommended callback to add components to an agent.
  * `Agent` - Created agent.
* `OnAgentBuild(Agent, Banner)` - Called after an agent is build and ready to be used but before it starts being used. This is the recommended callback for setting up spawned agents for the mission.
  * `Agent` - Built agent.
  * `Banner` - Banner of agent. Note that agents that do not have their own banners use banner of their team.
* `OnAgentShootMissile(Agent, EquipmentIndex, Vec3, Vec3, Mat3, bool, int)` - Called whenever an agent shoots a missile.
  * `Agent` - Shooter agent.
  * `EquipmentIndex` - Index of the weapon used. Note that for weapons that use another item as ammunition, like bows and crossbows, this is the index of the weapon, not ammunition.
  * `Vec3` - Starting position.
  * `Vec3` - Velocity of missile as a vector.
  * `Mat3` - Orientation of the missile. Note that this is not the direction of movement but the orientation of the missile itself.
  * `bool` - True if the missile has a rigid body.
  * `int` - Index of the missile. Seems to be only used to sync server and client and -1 if not coming from the server.
* `OnMissileCollisionReaction(Mission.MissileCollisionReaction, Agent, Agent, sbyte)` - Called after a missile reaction is calculated, generally after a missile hit.
  * `Mission.MissileCollisionReaction` - Calculated reaction.
  * `Agent` - Attacker agent. Can be null.
  * `Agent` - Defender agent. Can be null.
  * `sbyte` - Index of the bone missile attached to.
* `OnMissileHit(Agent, Agent, bool)` - Called whenever a missile hits something.
  * `Agent` - Attacker agent. Can be null.
  * `Agent` - Defender agent. Can be null.
  * `bool` - True if hit is canceled. Currently a hit is canceled when it is friendly fire and friendly fire is not enabled.
* `OnRegisterBlow(Agent, Agent, GameEntity, Blow, AttackCollisionData)` - Called after all the calculations for a hit is made.
  * `Agent` - Attacker agent.
  * `Agent` - Defender agent. Can be null.
  * `GameEntity` - Entity that has been hit. Can be null.
  * `Blow` - Information about the blow.
  * `AttackCollisionData` - Information about the attack. Also holds result of calculation.
* `OnAgentHit(Agent, Agent, int, int, int)` - Called whenever an agent is hit.
  * `Agent` - Agent that is hit.
  * `Agent` - Attacker agent. Can be null.
  * `int` - Calculated damage.
  * `int` - Weapon kind index of the weapon. Note that this is the kind index of missile for ranged weapons, not the weapon used to shoot it.
  * `int` - Weapon usage index of the weapon.
* `OnScoreHit(Agent, Agent, int, bool, float, float, float, AgentAttackType, float, int)` - Called whenever an agent is hit, right after `OnAgentHit`.
  * `Agent` - Agent that is hit.
  * `Agent` - Attacker agent. Can be null.
  * `int` - Weapon kind index of the weapon. Note that this is the kind index of missile for ranged weapons, not the weapon used to shoot it.
  * `bool` - True if the hit is blocked.
  * `float` - Calculated damage.
  * `float` - Damage bonus from relative movement speed of agents. This value is the multiplier giving just the bonus, for example 0.2 would mean 20% bonus damage from movement speed. Note that ranged hits do not have a movement speed bonus.
  * `float` - Distance of the ranged hit.
  * `AgentAttackType` - Type of the attack.
  * `float` - Difficulty of the shot. Calculated only for ranged hits.
  * `int` - Weapon usage index of the weapon.
* `OnAgentMount(Agent)` - Called when an agent mounts a mount.
  * `Agent` - Rider agent.
* `OnAgentDismount(Agent)` - Called when an agent dismounts a mount.
  * `Agent` - Rider agent.
* `OnAgentControllerChanged(Agent)` - Called when controller of an agent is changed.
  * `Agent` - Agent whose controller is changed.
* `OnItemPickup(Agent, SpawnedItemEntity)` - Called whenever an agent picks an item up.
  * `Agent` - Agent who picked up.
  * `SpawnedItemEntity` - Item that has been picked up.
* `OnFocusGained(Agent, IFocusable, bool)` - Called when an object gains the focus of an agent.
  * `Agent` - Seems to be always main agent.
  * `IFocusable` - Object that has gained the focus. For conversations, listener or speaker agent depending on who is talking. For other situations can be other agents, objects or mounts.
  * `bool` - True if the object that gained focus is interactable. Agents, mounts and usable objects seem to be interactable at the moment.
* `OnFocusLost(Agent, IFocusable)` - Called when an object loses its focus.
  * `Agent` - Seems to be always main agent.
  * `IFocusable` - Object that loses focus.
  * `Agent` - Interacting agent.
  * `Agent` - Target agent.
* `OnObjectUsed(Agent, UsableMissionObject)` - Called when an agent uses an object.
  * `Agent` - User agent.
  * `UsableMissionObject` - Used object.
* `OnObjectStoppedBeingUsed(Agent, UsableMissionObject)` - Called when an agent stops using an object.
  * `Agent` - User agent.
  * `UsableMissionObject` - Used object.
* `bool IsThereAgentAction(Agent, Agent)` - Called to determine if an agent is interactable by another agent. Note that any of the behaviours returning True will result in a True for final calculation.
* `OnAgentInteraction(Agent, Agent)` - Called when agent interacts with another agent. Currently seems to be called only when the target agent is human.
  * `Agent` - Interactor agent.
  * `Agent` - Target agent.
* `OnAssignPlayerAsSergeantOfFormation(Agent)` - Called when an agent is assigned as sergeant of the formation. Currently it seems be called only when a player is assigned as sergeant.
  * `Agent` - Sergeant agent.
* `OnAgentPanicked(Agent)` - Called when an agent is panicked. Currently, an agent starts fleeing when it is panicked.
  * `Agent` - Panicked agent.
* `OnAgentAlarmedStateChanged(Agent, Agent.AIStateFlag)` - Called when an agents alarm state is changed.
  * `Agent` - Agent whose alarm state is changed.
  * `Agent.AIStateFlag` - Added state flag.
* `OnGetAgentState(Agent, bool)` - Called when an agent's state after a killing blow is determined.
  * `Agent` - Agent whose state is determined.
  * `bool` - True if surgery is excersized. Seems to be used for granting experience to surgery.
* `OnEarlyAgentRemoved(Agent, Agent, AgentState, KillingBlow)` - Called when an agent's state change to something other than Active. Called before OnAgentRemoved.
  * `Agent` - Agent whose state is changed.
  * `Agent` - Agent causing the state change, e.g. attacker. Can be null.
  * `AgentState` - New state of the agent.
  * `KillingBlow` - Information about the blow if change was due to a hit.
* `OnAgentRemoved(Agent, Agent, AgentState, KillingBlow)` - Called when an agent's state change to something other than `Active`.
  * `Agent` - Agent whose state is changed.
  * `Agent` - Agent causing the state change, e.g. attacker. Can be null.
  * `AgentState` - New state of the agent.
  * `KillingBlow` - Information about the blow if change was due to a hit.
* `OnAgentDeleted(Agent)` - Called when an agent is about to be deleted. This is called after `OnAgentRemoved` callbacks.
  * `Agent` - Deleted agent.

## Others

* `OnAddTeam(Team)` - Called when a team is being added to a mission. Called before `AfterAddTeam`.
  * `Team` - Added team.
* `AfterAddTeam(Team)` - Called after a team is added to a mission.
  * `Team` - Added team.
* `OnFormationUnitsSpawned(Team)` - Called when units of a formation are spawned.
  * `Team` - Team this formation belongs to.
* `OnObjectDisabled(DestructableComponent)` - Called when an object is disabled. Currently seems to be called when a destructable object is destroyed.
  * `DestructableComponent` - Disabled object.

