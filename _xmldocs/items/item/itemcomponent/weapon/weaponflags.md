# WeaponFlags

## Parent Node

* [Weapon](./)

## Child Node

* _None_

## Attributes

[MeleeWeapon](weaponflags.md#meleeweapon) \| [RangedWeapon](weaponflags.md#rangedweapon) \| [HasString](weaponflags.md#hasstring) \| [StringHeldByHand](weaponflags.md#stringheldbyhand) \| [NotUsableWithOneHand](weaponflags.md#notusablewithonehand) \| [TwoHandIdleOnMount](weaponflags.md#twohandidleonmount) \| [AutoReload](weaponflags.md#autoreload) \| [UnloadWhenSheathed](weaponflags.md#unloadwhensheathed) \| [PenaltyWithShield](weaponflags.md#penaltywithshield) \| [WideGrip](weaponflags.md#widegrip) \| [CantReloadOnHorseback](weaponflags.md#cantreloadonhorseback) \| [Consumable](weaponflags.md#consumable) \| [UseHandAsThrowBase](weaponflags.md#usehandasthrowbase) \| [AmmoSticksWhenShot](weaponflags.md#ammostickswhenshot) \| [MultiplePenetration](weaponflags.md#multiplepenetration) \| [Burning](weaponflags.md#burning) \| [LeavesTrail](weaponflags.md#leavestrail) \| [CanPenetrateShield](weaponflags.md#canpenetrateshield) \| [MissileWithPhysics](weaponflags.md#missilewithphysics) \| [AmmoCanBreakOnBounceBack](weaponflags.md#ammocanbreakonbounceback) \| [AffectsArea](weaponflags.md#affectsarea) \| [AmmoBreaksOnBounceBack](weaponflags.md#ammobreaksonbounceback) \| [AttachAmmoToVisual](weaponflags.md#attachammotovisual) \| [CanBlockRanged](weaponflags.md#canblockranged) \| [HasHitPoints](weaponflags.md#hashitpoints)

* **MeleeWeapon**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon is a melee weapon_

* **RangedWeapon**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon is a ranged weapon_

* **HasString**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the ranged weapon has a string. Should be set to true for both Bows and Crossbows_

* **StringHeldByHand**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the string is held by hand. Should be set to true with Bows_

* **NotUsableWithOneHand**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon cannot be used in 1 hand_

* **TwoHandIdleOnMount**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _This is set to true with most bows and crossbows. TODO: figure out what this exactly does._

* **AutoReload**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If set to false an action is required to reload the weapon. \(crossbows\)_

* **UnloadWhenSheathed**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon should remove any loaded projectile when sheathed_

* **PenaltyWithShield**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon has a damage penalty when using with shield_

* **WideGrip**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _TODO: figure out what this does_

* **CantReloadOnHorseback**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon can be reloaded on horseback_

* **Consumable**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon can be consumed. Set to true for arrows and throwables._

* **UseHandAsThrowBase**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon is thrown from the hand_

* **AmmoSticksWhenShot**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _TODO: figure out what this exactly does_

* **MultiplePenetration**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the projectile can pierce through multiple entities_

* **Burning**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the projectile is on fire. TODO: figure out if this also inflicts fire damage, or sets fire to stuff_

* **LeavesTrail**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the weapon leaves a trail. TODO: figure out what this exactly does_

* **CanPenetrateShield**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If the projectile can penetrate a shield_

* **MissileWithPhysics**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If physics are attached to a projectile. TODO: figure out if this is used to damage props as well._

* **AmmoCanBreakOnBounceBack**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _TODO: figure out what this exactly does_

* **AffectsArea**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _TODO: figure out if this is AOE damage?_

* **AmmoBreaksOnBounceBack**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _TODO: figure out what this exactly does_

* **AttachAmmoToVisual**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _TODO: figure out what this exactly does_

* **CanBlockRanged**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If an item can block projectiles \(shields\)_

* **HasHitPoints**

  **类型:** `boolean`  
  **接受值:** `'true', 'false'`  
  **例子:** `true`  
  _If an item has hitpoints \(shields\)_

