# 寶可夢 藍版 Any% NSC 流程筆記

更新：2020 年 9 月 27 日


------

## 簡單介紹

過去的藍版 Any% NSC 流程和 RBA 一樣繁瑣，
需要跑到尼比市那邊用穿牆巫術 Brock Through Walls (BTW)，
還有一連串的道具溢出操作。

但在最新流程都精簡掉了，
利用角色名字、訓練師 ID 和特定寶可夢的個體值搭配夢幻漏洞就能進去殿堂，
甚至不需要叫出森林便利商店 (黃版)。

目前最有難度的操作是遊戲前的 TID 亂數控制，
4A Press 遇到烈雀和 2A Press 森林不遇敵，
需要熟練手順和 Buffer Input 技巧，搭配視覺提示在正確的位置上輸入指令。

另外補上進階的森林不遇敵，
2A Press

------

## 重要知識


<details>

### 開機流程

重新開機 -> Logo -> 公司 -> 流星 -> 胖丁 -> 標題 -> 標題選項
                                             -> 刪檔


### Hard Reset

快速上下撥動實機的電源開關，重新開機。


### Soft Reset 組合鍵

遊戲內的重開機功能，
「A + B + Start + select」


### 亂數調整

> 手動製造偶然的行為。

亂數調整是指降低遊戲隨機的方法，
目的在於減少運氣帶來的不確定性，
讓遊戲的流動控制在預想範圍內，
從而拿到稀有道具，或者更容易觸發特殊事件。

關鍵在於，亂數到底怎麼來的？
亂數是依據生成的規律準則——「亂數種子」演算而來，
通過不間斷的變換改變亂數種子，
讓遊戲產生出「看起來隨機」的亂數。


產生的規律準則——「亂數種子」，
亂數種子，


而 Reset 就是相當常見的方法之一，
通過重開機讓一切亂數歸零，



### Frame Window

Frame Window 可以理解為按鍵輸入時間的容錯程度，
計算單位是幀 (Frame)。

假設遊戲穩定維持在一秒 60 幀，
現在處理到第 30 幀 (半秒過去)，
那麼，16 Frame Window 就代表要第 31 ~ 46 幀這段期間按一下就好。

這個時候也可以換算成秒數來得到反應時間，
16/60 大約是 0.27 秒。


### Frame Perfect (1 Frame Window)

承上，1 Frame Window 就只能在第 31 幀這個瞬間輸入，
反應時間只有 1/60 大約是 0.017 秒。

而要求這麼離譜的技巧，
其難度認定稱為 Frame Perfect。

通常跑者會借助節拍器之類的工具輔助
(不是遊戲外掛而是真正意義上的節拍器)，
不過在藍版 Any% NSC 可以利用遊戲機制之一「緩衝輸入」，
來做到 Frame Perfect 這件事。


### 緩衝輸入 / Buffer Input

目的在於預先輸入指令，
讓遊戲「無縫」的接收指令，
不會因為閒置 1 幀而漏掉輸入，
浪費時間導致亂數失控。

而這種沒有任何時間損失，
亂數表現在預想範圍內的狀態，
就是我們所需要的 Frame Perfect。


### UsB 組合鍵 (上 + select + B)

在開機 Logo 之後的公司畫面期間輸入 UsB 組合鍵，
就可以快速跳過開場的流星和胖丁打架動畫。

在模擬器 Bizhawk 的輸入顯示中，
大寫 S 代表 Start 鍵，小寫 s 代表 select 鍵。


### 刪除存檔

另一方面，
在標題畫面輸入 UsB 組合鍵，
就會進入刪檔介面，選擇 Yes 就會砍掉舊紀錄。

這個舉動除了防止利用舊存檔作弊之外，
在最一開始的亂數調整套路也會經過這裡。

  
### 按到 A / A Presses

在大地圖上冒險時按到 A 會暫停世界 2 幀，
許多亂數調整要求一個或以上的 A Presses 操作。

這個部分可以參考筆記附有的路線圖，
利用畫面上的物件來當作視覺提醒，
在準確的位置、時機按下 A 鍵。

  
### 滅團起飛 / Deathfly

利用滅團觸發夢幻漏洞，
優點就是不用離洞繩 / 飛翔 / 瞬間移動等需要推進度才能實行。

</details>


------

## 排行榜 & 挑戰規則

<details>

### 排行榜

https://www.speedrun.com/pkmnredblue/full_game#Any_No_Save_Corruption


### 遊戲共通

暫無。


### 分類條件

- 投稿記錄必須附上影片證明。
- 挑戰採用 RTA 方式計時，
  按下 New Game 的時候開始計時；
  在破關畫面前，畫面全白的時候結束計時。
- 可以接受 S + Q (Saving and Quitting)。
- 投稿記錄必須使用英文版。
- 禁止損毀存檔。
- 其他遊戲漏洞 (trainer-fly，old man，之類的) 都可以使用。
- 禁止在還有存檔紀錄的情況下開新遊戲。
  你可以在標題畫面按「上 + Select + B」刪除存檔。
- 禁止 SFC 的 Super Game Boy (幀率不夠精確)。
- 可以接受 Super Game Boy 2。
- 禁止所有 Game Boy Tower (模擬不夠準確)。
- 唯一接受的模擬器是 gambatte-speedrun，
  必須使用最新版本 (目前是 r717)，搭配 GBC BIOS 開機。
- 其他模擬器一律禁止使用。
- 禁止使用模擬器的即時存檔、遊戲加速功能等等。
- 禁止使用自定義調色盤。
- 如果使用模擬器的話，至少要做到下面其中一項要求：
  1. 開始挑戰前先 Hard Reset 一次，
     之後投稿要保留這一段到紀錄影片中。
  2. 擷取整個視窗 (包含邊框)，像是這樣：
     ![](https://i.imgur.com/LTvx60r.png)

</details>


------

# 攻略流程


------

## 事前準備

- 使用模擬器的話，
  準備好 gambatte-speedrun r717 + GBC BIOS + 藍版 ROM (北美版)
- 在標題畫面輸入 UsB 組合鍵，
  進入刪檔介面把舊記錄砍掉
- 如果有投稿 RTA 記錄的需求，
  那麼在剪影片的時候要保留刪檔這一段


------

## [亂數調整] 訓練師 ID - 編號 61896


{%youtube u5_hDQ7H98w %}

- 利用 Buffer Input 取得理想的訓練師 ID
- 熟記開機流程，重溫一下相當經典的
- 以下步驟確保 Buffer Input 下進行
- 重點 & 視覺提示
  1. 先 Hard Reset 一次
  2. 在公司畫面按住 UsB 組合鍵，跳過流星和胖丁動畫
  3. 在標題畫面按住 UsB 組合鍵，即將進入刪檔介面
  4. 進去前的這個瞬間，馬上去按 Start + select + A + B，
     文字框顯示一下 C，之後就會 Soft Reset
  5. 先不要動，等到胖丁動畫，胖丁第一次跳躍時按 A 跳過
  6. 標題畫面按 Start 即將進入標題選項介面
  7. 進去前的這個瞬間，馬上去按 B 退回標題畫面
  8. 回到標題先不要動，
     等到傑尼龜完全離開畫面後、手上的精靈球彈起來的時候按 Start
     (RNG 正確的話會出現飛腿郎，出現臭臭花或是其他寶可夢都會失敗)
  9. 選項畫面前按 A 開新遊戲，
     按下 New Game 的時候開始計時


------

## Bizhawk 2.5.1

- 記憶體位置: System Bus - 0xD359 (2 Bytes, Hex, Big Endian)
- SubGBHawk / Console - GBC / CGB in GBA
- Gambatte / Offical BIOS / Console - GBC / CGB in GBA


------

## 設定


### 角色取名

- 主角 m <sup>M</sup><sub>N</sub> a . ♀️ t F (總共 7 個字元)
- 宿敵選預設名字 RED


### 進入遊戲

- 系統選項 Fast / Off / Shift


------

## 真新鎮

- 馬上出鎮，結果被博士攔截到研究所
- 領取最左邊的小火龍 (Charmander)，不用命名
- 按 Start 打開選單 -> 查看隊伍中的小火龍 -> 檢查訓練師 ID
- 理想的訓練師 ID (Trainer ID，TID)
- 目標 TID: 61896 (F1C8)
- 錯誤的話砍存檔重新來過；正確的話先存檔，再去打架
- 宿敵戰輸贏不重要


## 送貨事件

> 任務期間遇敵就逃跑，不要練等

- 離開真新鎮研究所，往上走經過 1 號道路前往常磐市
- 常磐市超商取貨之後回到真新鎮研究所
- 完成送貨事件後，再次前往常磐市


## 常磐市 - 便利商店

- 購買
  解毒藥 (Antidote) * 1
  精靈球 (Poké Ball) * 14
- 離開超商，往左走到 22 號道路


------

## [亂數調整] 烈雀 - 個體值 FEF1

{%youtube Juvj2kGndfo %}

- 抓一隻個體值為 FEF1 的 烈雀 (Spearow)
- 如何判斷是正確結果：定點相遇
- 重點
  (1) 在指定位置存檔，然後 Hard Reset
  (2) 重開機之後的 Logo 期間按一下左鍵改變調色盤
  (3) 全程緩衝輸入
  (4) 不能走錯路線
  (5) 特定位置按 A
  (6) 命名：AA
- 改變調色盤：
- 全色盲判定：近白背景 & 近黑文字 -> 淺灰背景 & 深灰文字


------

## 常磐市 - 寶可夢中心

- 寄放小火龍到電腦寄放系統
- 恢復體力 (設置傳送點)
- 往上走經過 2 號道路前往常磐森林
- 遇敵就逃跑，不要練等


------

## [亂數調整] 皮卡丘定點相遇

{%youtube UxsOKYi_Nzs %}

- 重點
  1. 在指定位置存檔，然後 Hard Reset，之後全程緩衝輸入
  2. Logo 期間按「左」改變調色盤
  3. 不要走錯路線
- 讓皮卡丘打爆烈雀，發動滅團起飛


------

## 剩下步驟

- 再次前往常磐森林，進去後馬上二連戰
- 烈雀啄好啄滿
- 二連戰後會進入巫術狀態，走路、觸發對話變慢
- 往右走與昆蟲少年對話，進行戰鬥
- 成功的話，戰鬥結束後會進入殿堂 (關燈)
- 在破關畫面前，畫面全白的時候結束計時，GG


------

## 進階部分 & 細節研究

- B 鍵按住文字框會保持在高速顯示狀態，然後 A 鍵連打推進對話

- 繞到大木博士背後對話，宿敵提早出現

- [亂數調整] 森林不遇敵 (進階)

{%youtube wmnWBtQiLag %}

- 特定位置按 A (2 個)：
  (1) http://pokeworld.herokuapp.com/rb/51#25,26
  (2) http://pokeworld.herokuapp.com/rb/51#20,9

- (選) 戰鬥期間保持 Buffer Input 將會一發捕捉烈雀 (Yoloball)

### 一發捕捉 / Yoloball

保持緩衝輸入狀態，
讓遇敵到拋球整個過程沒有閒置，
就會一發捕捉寶可夢。
難點在於「野生寶可夢出現辣！」這個提示框，
必須在 4 幀時間內按掉 (通常會 A -> B 鍵刷過去)。

更重要的是，不要屈服於無腦連打的誘惑！

- DVs (Determinant Values)：英文圈在第一、二世代的個體值稱呼


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


Pokemon NSC 2015 Route - HackMD
https://hackmd.io/TCUNwlQkQUGYj1Icv0r9nw
Append 提供的黃版 NSC 2015 年版攻略翻譯 + 註解

Dabomstew/gambatte-speedrun - GitHub
https://github.com/Dabomstew/gambatte-speedrun
Fork of https://github.com/sinamas/gambatte with Pokémon speedrunning-related changes

Pokémon Blue NSC full Beginner Guide UPDATED - Google 文件
https://docs.google.com/document/d/1l10apKvZgTeOSEKeuhgHVGC73z9-f2FTkuUKHZaPVEA/edit
krazyd4n 在 Speedrun.com 排行榜的攻略區發表的新手指南

Pokémon Blue Any% No Save Corruption Guide by davidpoko - Google 文件
https://docs.google.com/document/d/14Vep4XZ-46nNPb5r2bK3QNut6G8DHzwe8tkZyTZnJrU/edit
上一篇教學的重點整理，相當簡潔

Why do we need to manipulate the trainer ID ? - Speedrun.com
https://www.speedrun.com/pkmnredblue/thread/c2p8x
訓練師 ID 亂數調整的相關討論

RNG manip on GBC - Speedrun.com
https://www.speedrun.com/pkmnredblue/thread/jpbib
實機與模擬器的 RNG 討論

Pokémon Red/Blue/RNG Manipulation FAQ - Pokemon Speedruns Wiki
http://wiki.pokemonspeedruns.com/index.php?title=Pok%C3%A9mon_Red/Blue/RNG_Manipulation_FAQ
簡單介紹第一世代的亂數控制

[GB / GBA] 寶可夢 藍版 - Any% NSC (Emu) in 13m 44s - Speedrun.com
https://www.speedrun.com/pkmnredblue/run/yj49w9ny
幾天下來的研究 + 練習的成果，
過程中多次遇敵拖到時間，
但成功做到 6 次 A Press (+ Yoloball)！

Pokemon Blue - Any% NSC in 13m 36s (RTA) by Spiraster - Youtube
https://youtu.be/79-xyJZ6TVM
擁有全程輸入顯示的 RTA 記錄影片


------

## Thanks for watching :)

{%hackmd @nto84543/B1BnP1CSw %}


------

