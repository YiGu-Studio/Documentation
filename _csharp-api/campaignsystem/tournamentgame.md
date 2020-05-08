# （中世纪的）比赛 - TournamentGame

此类用于处理比赛的参与者和固有设置，要修改某些行为，可能需要一个`Harmony补丁`

注意：此页面不完整，因此，如果您发现有关此主题的更多信息，请创建请求请求并添加到此不断增长的Modding文档中！

## 可访问的方法

> `protected TournamentGame(Town town, ItemObject prize = null)`

在`AddTournament`和`CreateTournament`方法之后被调用的内部方法，用来设置奖品

## 可访问的属性

|属性名|描述|
|--|--|
|public const int `ParticipantNumber`|参加人数，目前已硬编码为16，但可以修补|
|public Town `Town`|比赛所在地|
|public CampaignTime `CreationTime`|比赛的创建时间|
|public QualificationMode `Mode`|资格模式“TeamScore（团体得分）”或“ IndividualScore（个体得分）”均可更改|
|public virtual int `MaxTeamSize`|比赛每个阶段的团队人数上限|
|public virtual int `MaxTeamNumberPerMatch`|在比赛的每个阶段中，每场比赛的最大团队数|
|public ItemObject `Prize`|比赛的奖金|
|public virtual float `TournamentWinRenown`|赢得比赛赢得了声誉|
|public static List\<CharacterObject\> GetParticipantCharacters(Settlement `settlement`, int `maxParticipantCount`, bool `includePlayer` = true, bool `includeHeroes` = true )|此方法定义比赛开始时的参与者,在玩家参加比赛或模拟比赛时调用|
|public abstract TextObject GetMenuText()|加入比赛时，此方法定义菜单上的文本|
|public abstract void OpenMission(Settlement `settlement`, bool `isPlayerParticipating`)|在开始比赛/模拟时有玩家参与时调用此方法|
|public void PrepareForTournamentGame(bool `isPlayerParticipating`)|在开始比赛/模拟时有玩家参与时调用此方法|
