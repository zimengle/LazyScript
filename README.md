# LazyScript

基于 [LazyScript](https://github.com/laytya/LazyScript) 改造

## 关于我

我是一名狂热魔兽怀旧服玩家，也是一名9年百度 3年腾讯的程序员，目前在玩欧服乌龟服，喜欢折腾各种插件 自动化，如果你也是一名喜欢打魔兽的程序员，联系我email:30962088@qq.com，一起玩

## 为什么要做这个项目

我在玩战士 需要在敌人闪躲之后切换战斗姿态进行压制，发现里面有一些bug，还有没有最中文的支持。


## 以下是我的做一些宏

### 战士

#### 输出

* 通用狂暴战

```
-- 战斗怒吼
battleShout-ifNotPlayerHasBuffTitle=战斗怒吼
-- 优先使用压制
overpower
-- 嗜血
bloodthirst
-- 如果是战斗姿态，英勇泄怒
heroicStrike-ifStance=battle
-- 狂暴姿态
berserk-ifInCombat-ifPlayer<26rage
-- 斩杀
execute-ifTarget<20%hp-ifInCombat
-- 旋风斩
whirlwind
-- 英勇打击
heroicStrike-ifPlayer>59rage
-- 自动攻击
autoAttack
-- 闪躲成功且压制冷却 怒气在4-28之间切换武器姿态
battle-ifPlayer<28rage-ifPlayer>4rage-ifTargetDodged-ifNotInCooldown=overpower
```

* aoe
```
-- 战斗怒吼
battleShout-ifNotPlayerHasBuffTitle=战斗怒吼
-- 狂暴姿态
berserk-ifNotStance=berserk
-- 优先斩杀
execute-ifTarget<20%hp-ifInCombat
-- 旋风斩
whirlwind
-- 顺劈斩
cleave-ifPlayer>45rage
-- 自动攻击
autoAttack
```