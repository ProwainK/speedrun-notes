# 寶可夢 TCG Any% ACE 流程筆記

更新：2020 年 2 月 2 號


------

## 簡單介紹

巫師 gifvex 和 entrpntr 的巫術抓漏再次發威！

寶可夢 TCG Any% 在 2020 年 1 月期間，
新巫術「中斷決鬥」橫空出世，
只用到 13 分 36 秒就能破關 (by 000aj)，
相較於 Any% Glitchless 節省了多達 33 分鐘。

而到了 2 月初發現了「中斷決鬥」的進階應用，
現在很可能在 4 分鐘內便可結束！

首先將牌組按特定順序整理，
再利用 Soft Reset 重整系統亂數。

此時會用上 FlowTimer，
這是一款針對寶可夢系列作品設計的倒數計時軟體，
輔助玩家取得理想的 RNG。

藉由亂數控制出固定發牌，
搭配「中斷決鬥」，
就可以把我們帶到破關名單。


------

## 中斷決鬥 (Duel Escape)

https://old.reddit.com/r/speedrun/comments/eqrucd
https://www.youtube.com/watch?v=ieyYHsurOcQ
https://www.speedrun.com/pkmntcg/guide/52pes

gifvex 和 entrpntr 發現了這個巫術：

在場上選擇最後一張卡的同時輸入「下 + A」，
遊戲就會去讀取下面的空格欄，也就是一張無效卡；

讀取那張無效卡就會有 50% 機率立即獲勝。


------

## FlowTimer 設定


------

## 教學戰、選牌組和系統設定 

* 教學戰用中斷決鬥 Skip 掉
* 選擇牌組「Squirtle & Friends Deck」
* 暫停選單 -> Config
  * Message Speed：5
  * Duel Animation：None


------

## 整理牌組

> 接下來要按順序整理牌組，
  可以先存檔。
  
* 暫停選單 -> Deck -> 第一副牌組 -> Modify Deck，準備開始整理牌組

[左] +Grass Energy
[右] +Kakuna
[右] +Arcanine
[左左] -Water Energy x3, +Water Energy, +Lightning Energy
[左] -Professor Oak, -Bill, +Bill, -Switch, +Switch, -Poke Ball

* 儲存牌組，儲存遊戲


------

## 亂數控制

* Soft Reset + FlowTimer 倒數計時
  (Offset 設定為 22700) (22550 + 150)
* 前往 Science Club (右右上上)
* the deck shuffle you're aiming for is 2nd textbox after saying yes to the duel
* 雙方牌組順序會在接受決鬥之後，
  第二個對話框按下去時就完成決定


### 手牌確認表

-6 : Scoop Up, Abra, Grass, Meowth, Full Heal // Psychic, Abra
-5 : Potion, Switch, Water, Gastly, Psychic // Staryu, Seel
-4 : (x2) Water, Starmie, Water, Psychic, Water // Squirtle, Seel
-3 : Haunter, Water, Grass, Psychic, Kakuna // Psychic, Machop
-2 : Kadabra, Psychic, Machop, Gastly, Kakuna // Squirtle, Starmie
-1 : Water, Fighting, Bill, Fighting, Water // Squirtle, Geodude

0 -> Fightzzzzing, Seel, Fighting, Fighting, Staryu // Raticate, Seaking

+1 : Fighting, Rattata, Water, Potion, Fighting // Abra, Psychic
+2 : Water, Water, Fighting, Bill, Geodude // Rattata, Psychic
+3 : (x1) Gastly, Seel, Psychic, Water, Psychic // Raticate, Fighting
+4 : Scoop Up, Seel, Fighting, Abra, Rattata // Water, Psychic
+5 : (x1) Starmie, Rattata, Geodude, Water, Rattata // Squirtle, Psychic
+6 : Full Heal, Rattata, Fighting, Water, Lightning // Squirtle, Psychic


> 手牌不對就再來一次 Soft Reset + FlowTimer 倒數計時


------

## 中斷決鬥

* 派出 Seel 和 Staryu，放到場上
* 一定會是我方先攻，馬上結束這回合
* 對方攻擊會使用 Whirlwind
* 當要求玩家選擇寶可夢時，按兩次 Select
* 畫面會轉到場面上的時候，可以嘗試發動巫術「中斷決鬥」
* 中斷成功 + 前面都 Set 好的話，就會跳到破關名單


------

## 特別感謝

感謝 **gifvex** 和 **entrpntr**，
巫術「中斷決鬥」以及進階應用都出自於這兩位巫師，
大幅推進寶可夢 TCG Any% 的 Speedrun 流程。

感謝 **tikevin83**，
除了會在討論區分享資訊外，
親身投入實戰驗證套路、整理筆記真的受益良多。


Shoutout to **gifvex** & **entrpntr**,
who hunting this powerful glitch and writing clean guide.

Also **tikevin83** who share many useful PM TCG Any% info :)

------

https://www.speedrun.com/pkmntcg#Any

https://old.reddit.com/r/speedrun/comments/exk44m
https://pastebin.com/rm8z7U4B
https://youtu.be/mhshmaSITPc

https://github.com/stringflow/FlowTimer

------

