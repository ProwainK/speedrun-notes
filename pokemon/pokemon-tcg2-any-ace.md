# 寶可夢卡片 GB2 Any% ACE 流程筆記

更新：2020 年 2 月 7 號

------

## 遊戲資訊

<details>

### 名稱

寶可夢卡片ＧＢ２：ＧＲ團參上！
Pokemon Card GB2: Here Comes Team GR! / Pokemon TCG2
ポケモンカードＧＢ２：ＧＲ団参上！

### 主機

GBC

### 版本 & 年份

日版 in 2001

</details>


------

## 挑戰規則

<details>

### 遊戲共通

暫無。

### 分類條件

* 挑戰採用 RTA 方式進行計時。
  在角色創建完成，選下「はい」的時候開始計時；
  在破關名單前，進入白幕轉場的時候結束計時。
* 可以接受 S+Q (Saving and Quitting)。
* 可以接受粉絲製作的英語翻譯版本。
* 英文卡表必須使用 Artemis251 製作的 Patch：
  http://www.romhacking.net/translations/1736/
* 禁止 SGB in SFC (幀率不夠精確)。
* 可以接受 Super Game Boy 2。
* 唯一接受的模擬器是 gambatte-speedrun，
  必須使用最新版本 (目前是 r664)，並且使用 GBC BIOS 開機。
* 其他模擬器一律禁止使用。
* 禁止使用模擬器的即時存檔、遊戲加速功能等等。
* 禁止使用自定義調色盤。
* 如果使用模擬器的話，至少要做到下面其中一項要求：
  1. 開始挑戰前先 Hard Reset 一次，
     之後投稿要保留這一段到紀錄影片中。
  2. 擷取整個視窗 (包含邊框)，像是這樣：
     ![](https://i.imgur.com/LTvx60r.png)

</details>


------

## 重要技巧

<details>

### 決鬥中離 / Down+A Glitch

決鬥中離 (Down+A Glitch)，
觸發這個巫術之後會有機率馬上離開決鬥，
又稱 Duel Escape Glitch。

PSR (Pokemon Speedrun) 社群的兩位巫師 gifvex 和 entrpntr，
在 GBC 上的 TCG 1 代發現了這個巫術：

{%youtube ieyYHsurOcQ %}

先按 Select 去觀看整個場地，
把鼠標移到自己場地裡的最後一張卡片，
在這個時候同時輸入「下 + A」，
遊戲就會去讀取下一個空格欄，也就是一張無效卡；

「**讀取那張無效卡就會有 50% 機率馬上中離並且獲勝**」。

中離效果很類似於新仙劍奇俠傳的金蟬脫殼 Bug，
不過這邊有比較嚴格的輸入要求，
系統必須在同一幀收到「下 + A」。

然而在 GBC 上會有 Lag Frames 的情況發生，
需要讓系統暫停、Lag 一下來處理計算，
這個瞬間玩家還是能夠輸入指令，
這個技巧稱為緩衝輸入 (Buffer Input)。

以致於決鬥中離這個巫術，
並不要求 Frame Perfect。

決鬥中離在 TCG 2 代也能奏效，
搭配特定操作就做到了 ACE，
從決鬥中離開並跳到破關名單畫面。

值得注意的是，如果沒有馬上中離，
就會卡在隊伍狀態畫面，
就算按 B 關掉也會自動打開。

實際上這樣更容易操作，
按 B 關掉之後有更多的 Lag Frames；
在 TCG 2 代 ACE 的最後階段，
必須要在這個瞬間緩衝輸入「下 + A」達成二次觸發。

</details>


------

## 攻略流程

### 事前準備

* 使用模擬器的話，
  準備好 gambatte-speedrun r664 + GBC BIOS
* 開始挑戰前先 Hard Reset 一次，
  之後投稿要保留這一段到紀錄影片中
* 在角色創建完成，選下「はい」的時候開始計時

### 開場動畫

* 等過場之後拿到牌組
* 暫停選單 -> 設定 (せってい)
  * 文字速度 (メッセージの はやさ)：5
  * 對戰動畫 (対戦 アニメーション)：みない
  * 擲硬幣動畫 (コイントス アニメーション)：スキップあり

### 牌組命名

* 依照順序修改牌組名字：

按 B 四次清掉，保留最後一個字「さ」
づ：A，Start，左，[上 + A]
s：下，A，Start，右，下，[下 + 左]，[下 + 右 + A]
H：Start，[左 + A]，右，[下 + A]
ァ：左，上，左，[上 + A]
ゥ：下，右，[上 + A]
C：下，左，左，[下 + A]
R：Start，下，[下 + 左]，[右 + A]
h：Select，Start，[下 + A]
-：左，下，左，下，[下 + 右 + A]

* 牌組取名為「さづsHァゥCRh-」，
  改名完成

### 兩次決鬥中離

* 到牌桌邊與助手對話，先選「いいえ」拒絕一次
* 再對話一次，選擇「ふつうに対戦」進入戰鬥
* 召喚地鼠到場上後，按 Select 觀看整個場地
* 這個時候先同時輸入下 + A，觸發決鬥中離，
  成功的話會看到草系能量卡
* 此時按 B 取消，瞬間接著輸入 (刷鍵去按) 下 + A，
  再觸發一次決鬥中離
* 在破關名單前，進入白幕轉場的時候結束計時


------

## ACE 細節原理

### 牌組命名

首先要修改牌組的名字，
系統就會把文字轉換成數值，
並且從記憶體中 D2E0 這個區域開始順序放置。

記憶體位置 | 輸入                    | 文字變數值
-----------|-------------------------|------------
D2E0       | s                       | 04 3C
D2E2       | づ                      | 0E 4A
D2E4       | ズ                      | 0F 45
D2E6       | R，h                    | 04 21 04 31
D2EA       | b                       | 04 2B
D2EC       | Grass                   | 05 02
D2EE       | 9，然後把 9 砍掉        | ?? -> 00 69

### 暫存器 HL

現在，GBC 有兩個暫存器 H 和 L，
通常會合在一起稱為暫存器 HL，
它們負責存放記憶體的位置資料。

CPU 會從暫存器 HL 得知任務地點，
然後就會跑過去開始執行指令。

### 決鬥中離

觸發兩次決鬥中離會讓系統在一番折騰之後，
讓暫存器 HL 給出 D0D2，
讓 CPU 前往這個區域執行指令。

而 D0D2 區域是用來暫時保存我們整理牌組專用，
然而這涵蓋到改牌組名字用的 D2E0 區域。

因為我們只有修改牌組名稱，沒有更動其他地方，
所以 D0D2 區域 (D0D2 ~ D2DF) 都沒有指令而讓 CPU 空轉，
一直到 D2E0 區域。

### 這個時候會發生什麼事？

CPU 會把牌組名字當成 CPU 指令來執行！
接下來，就是見證奇蹟的時刻。

數值        | 數值變 CPU 指令
------------|-----------------
04 3C       | inc A
0E 4A       | load 4A into C
0F 45       | rotate A and load L into B
04 21 04 31 | inc B and load 31 into H
04 2B       | inc B
05 02       | dec B and load A into (BC)
00 69       | load C into L

We write "jump (HL)" to D34A (using register A), then set HL to 314A.

> 這段真的看不懂，我的理解是：
> 
> 1. CPU 會利用暫存器 A，
>    將「暫存器 HL 給我粉」這個指令放到 D34A
> 2. 把暫存器 HL 存放的記憶體位置設定為 314A
> 
> 僅供參考。

最後，系統就會跑去 314A 區域執行指令，
剛好 314A 區域有我們想要的數值，
「觸發破關名單畫面」。


------

## 心得 & 感謝

第一次深入去了解到硬體底層，
用到 Bizhawk 的 Debugger 來搞懂運作原理...
最困難的是，把艱澀內容整理成筆記 (Nani the fuxk)。

實際上最後的數值變 CPU 指令那一 Part 還是理解不能，
幸好實際去 ACE Setup + 觸發巫術相當容易上手，
可能哪天功力提升，有機會回頭研究再來挑戰吧。

感謝 Blazephlozard，
除了投入改良套路，甚至製作出 TAS！
更重要的是，整理出攻略指南讓我成功學到 ACE 套路破關。

另外還有 gifvex 和 entrpntr，以及 PSR 社群提供的資源～

Shout out to Blazephlozard's guide and TAS;
Also gifvex, entrpntr and PSR Community,
who researched and provided this insane glitch :)


------

## 參考資料

Speedrun.com 排行榜
https://www.speedrun.com/pkmntcg2#Any
記錄寶可夢 TCG2 Any% ACE 的成績排行榜

Speedrun.com 教學區攻略指南
https://www.speedrun.com/pkmntcg2/guide/twr5y
跑者 Blazephlozard 製作的簡易攻略，其中提及到 ACE 的細節原理

Duel Escape Glitch 展示影片
https://youtu.be/ieyYHsurOcQ
由 entrpntr 製作，提供輸入操作給玩家参考

2m 05s by Blazephlozard
https://youtu.be/E1AmrLNlvss
相當有魄力的成績，隨著巫術開發，TCG2 從一小時多壓到兩分鐘便可結束

gambatte-speedrun 模擬器
https://github.com/pokemon-speedrunning/gambatte-speedrun/releases
PSR (Pokemon Speedrun) 社群針對第一、二世代的 RNG 表現而改良調整的一款模擬器，
請下載最新版的 Release 6, Build 664，
檔案名字是「gambatte-speedrun-r664-psr.zip」

GBC 硬體一覽
https://fruttenboel.verhoeven272.nl/Gameboy/GBsummary.html
從 CPU 指令到記憶體都是 ACE 不可或缺的一部份。

http://tasvideos.org/6622S.html


------

## Thanks for watching :)

<style>
#doc {
  font-family:
    monospace,
    monospace,
    'MotoyaLMaru W3 mono',
    sans-serif !important;
}
</style>


------

