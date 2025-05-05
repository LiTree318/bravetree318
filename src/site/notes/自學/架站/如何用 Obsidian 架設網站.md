---
{"title":"🔖 如何用 Obsidian 架設網站","dg-publish":true,"tags":["DigitalGarden","obsidian","self_learing","website_design","🎯學習歷程檔案"],"status":"🪲 Bugs","permalink":"/自學/架站/如何用 Obsidian 架設網站/","dgPassFrontmatter":true,"created":"2025-05-05T18:30:31.468+08:00","updated":"2025-05-05T23:55:55.232+08:00"}
---


> [!warning] README 👈 請先讀我
> 1. 這份文件完全基於 [Wanderloots's Words](https://wanderloots.xyz/) 分享的 [Digital Garden 說明](https://wanderloots.xyz/digital-garden/tutorials/how-to-publish-obsidian-notes-website-for-free-digital-garden-or-blog/)，部分參考[oleeskild](https://github.com/oleeskild/obsidian-digital-garden)架設的[另一個 Digital Garden 說明](https://dg-docs.ole.dev/)[^1]。 
> 2. 此外，這份文件（以及本網站）的所有github檔案皆使用自[oleeskild設定好的 Digital Garden 檔案](https://github.com/oleeskild/digitalgarden)，感謝每一位網路大神無私奉獻 🙏。   
> 3. 最後，本人完全沒有任何網頁架設和程式設計的底子，若有任何錯誤（或者bug）歡迎來信指正，我們一起研究、一起學習！以下是我的聯絡信箱：
>    📪 `tree10zi23@gmail.com`


## ⚒️ 事前準備


> [!tip] 架站之前請先準備以下幾項工具：
>  - [ ] 下載 [Obsidian](https://obsidian.md/)，並建立一個屬於自己的 Obsidian 儲存庫（Vault）[^2]
>  - [ ] 在自己的儲存庫裡面新增一些筆記
>  - [ ] 擁有一個自己的 [Github](https://github.com/) 帳號，如果沒有的話，請先[註冊](https://github.com/signup?source=header-repo&source_repo=LiTree318/bravetree318)
>  - [ ] 此外，我將會使用 Netlify 作為托管資料和生成網域的平台[^3] （更多詳細介紹，請參考註腳[^3] ）


## 🎯 步驟一：建立儲存庫，並開啟一些筆記。

1. Obsidian 官網下載軟體
2. 安裝軟體後建立自己的儲存庫
3. 隨意寫幾個筆記（請先至少寫兩個作為測試）


## 🎯 步驟二：建立 Github，並且與儲存庫串連

> [!tip] Github 的用途
> 我們使用Github的原因，是為了將我們在電腦上的文件可以同步到網路，同時方便我們移轉到 Netlify 呈現成網頁。

#### （一） 登入（註冊）一個 Github 帳號

- 註冊／登入 Github
- 接下來，到Setting設定自己的 **密鑰** （token key）→ ==這部份是個人隱私，請注意！==
#### （二）取得 **密鑰**

- 點選 **Generate new token (classic)**


- **Note** 隨便打文字，讓自己知道這是此次生成的 **密鑰**。
- **Expiration** 設定 **密鑰** 的使用時間，可以維持最低日期 30 天。
- **Select scopes** 將 `repo` 點開，以便可以提供其他裝置使用。
- 到最底下綠色方框，點選 **Generate token**。
- **紅色方框處** 就是您生成的 token。
- ⚠️ **請記得，這份token只會在這裡出現一次，請務必複製好！！！**
 
![[Pasted image 20250505210614.png]]

#### （三）回到 Obsidian，開啟社群外掛，安裝「Digital Garden」

#### （四）建立「Digital Garden」模版

- 從外掛「Digital Garden」分享[網頁模版](https://github.com/oleeskild/digitalgarden)
- 並將該模版複製到您的Github帳號中
- 成功之後，在您的專案會有您方才複製並新增的Repo（以下簡稱專案）
#### （五）將儲存庫和專案綁訂（Obsidian – Github）

- 點開第三方外掛程式，設定「Digital Garden」，將畫面中紅、綠、藍的格子填入內容（直到上方 ❌ 變成 ✅ ）
- 密鑰在上方第（二）點。

![[Pasted image 20250505213119.png]]

## 🎯 步驟三：登入 Netlify 並呈現網頁

#### （一）打開 Netlify，註冊／登入帳號
- 選擇用 Github登入
![[Pasted image 20250505213722.png]]
#### （二）新增網站，將資料從 Github 匯入
- 第一次使用需要授權 Netlify 和 Github 串連。

![[Pasted image 20250505213827.png]]
- 選擇下方的「**Can’t see your repo here? Configure the Netlify app on GitHub.**」，從這裡設定授權。
![[Pasted image 20250505213843.png]]


- 選擇下方「Repository access」，將您方才設定的專案授權給 Netlify。

![[Pasted image 20250505214021.png]]
- 此時，您的首頁上會出現方才加入的專案。

![[Pasted image 20250505214124.png]]
- 點開，在下方輸入網域名稱（記得不要重複，此處之後可以改），然後送出。
![[Pasted image 20250505215344.png]]

#### （三）進入 Obisidan，對您剛才新增的筆記進行調整
- 每個筆記前端需要加上下面的指令：

```YAML
---
title:
dg-home: 
dg-publish:
tags:
- "測試用"
---
```

這邊有幾行指令，以下進行簡單的說明（更詳盡關於指令的介紹，以後會補充）。

- 首先，這些指令「一定要加在文件最上方」，從行號 1 開始；
- `---` 夾起來的區域代表「這個文件的屬性」，後續，可以在這裡客製每一份筆記的內容。
- `title` 是這篇筆記的「標題」，在這裡設定的標題會是「最終」網頁呈現的網頁標題。
- `dg-home` 代表這篇筆記是您網頁的「首頁」；既然是首頁，代表您整個儲存庫應該只會有這一份筆記有這個文字。請在 `:` 後面輸入 `True`，代表這份筆記「是首頁」。
- `dg-publish` 代表這篇筆記「會匯出到網頁」。每一份筆記都需要加上這一段文字，才能匯出到網頁上（相反的，如果儲存庫中的筆記沒有加上這一行，就無法匯出到網站上）。請在 `:` 後面輸入 `True`，代表這份筆記要上傳。
- `tags` 可以輸入標籤，用來分類每一份筆記，用法如上。

![[Pasted image 20250505215011.png]]
![[Pasted image 20250505215048.png]]


#### （三） Digital Garden，啟動！打開 Netlify，檢查網頁是否匯出成功

![[Pasted image 20250505215435.png]]


其他參考 [[私人筆記/整理中/我的求救訊息\|我的求救訊息]]

[[🌲 HERE IS THE TREE'S HOLE\|🌲 HERE IS THE TREE'S HOLE]]

[^1]: 這部份特別感謝[邱佳昇支援](https://www.facebook.com/share/p/16YThn4q9h/)，讓我可以按圖索驥找出自己的bugs（2025年5月5日）。
[^2]: 由於我是使用全英文介面的 Obisidn（為了用快捷搜尋），因此之後本分文件所有用到的vault會統一用「儲存庫」來翻譯（這也是官方中文給定的譯名）。
[^3]: [Wanderloots](https://wanderloots.xyz/digital-garden/tutorials/how-to-publish-obsidian-notes-website-for-free-digital-garden-or-blog/) 和 [oleesklid](https://dg-docs.ole.dev/getting-started/01-getting-started/) 有針對其他托管平台（Vercel）進行說明。但我將只以 Netlify 做介紹，以方便統一使用工具。