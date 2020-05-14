# ChangeOwnerOfSettlementAction 类

这个类中的函数是用来设置或者更改定居点拥有者的.

## 函数

以下列表罗列了通过不同方法来更改定居点拥有权的函数:
- `ApplyByDefault(`[Hero](../hero.md)	`hero, `[Settlement](../settlement.md)`settlement)` - 在开始战役或者玩家启用作弊获取定居点时启用
- `ApplyByKingDecision(`[Hero](../hero.md)`hero, `[Settlement](../settlement.md)`settlement)`
- `ApplyBySiege(`[Hero](../hero.md)`newOwner, `[Hero](../hero.md)`capturerHero, `[Settlement](../settlement.md)`settlement)`
- `ApplyByRevolt(`[Hero](../hero.md)`hero, `[Settlement](../settlement.md)`settlement)`
- `ApplyByLeaveFaction(`[Hero](../hero.md)`hero, `[Settlement](../settlement.md)`settlement)`
- `ApplyByBarter(`[Hero](../hero.md)`hero, `[Settlement](../settlement.md)`settlement)`
- `ApplyByRemoveFaction(`[Settlement](../settlement.md)`settlement)`
- `ApplyByDestroyClan(`[Settlement](../settlement.md)`settlement, `[Hero](../hero.md)`newOwner)` - 定居点的拥有者在死亡后其采邑将随机分封给前任拥有者的子嗣.
