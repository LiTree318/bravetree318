---
{"title":"🔖 如何用 Obsidian 架設網站","dg-publish":true,"tags":["DigitalGarden","obsidian","self_learing","website_design"],"type":["🎯學習歷程檔案"],"permalink":"/publish/website-building/obsidian/","dgPassFrontmatter":true,"noteIcon":"","created":"2025-05-05T18:30:31.468+08:00","updated":"2025-05-05T18:50:35.379+08:00"}
---


# 🔖 如何用 Obsidian 架設網站

> [!warning] README 👈 請先讀我
> 1. 這份文件完全基於 [Wanderloots's Words](https://wanderloots.xyz/) 分享的 [Digital Garden 說明](https://wanderloots.xyz/digital-garden/tutorials/how-to-publish-obsidian-notes-website-for-free-digital-garden-or-blog/)，部分參考[oleeskild](https://github.com/oleeskild/obsidian-digital-garden)架設的[另一個 Digital Garden 說明](https://dg-docs.ole.dev/)[^1]。   
>     <br>
> 2. 此外，這份文件（以及本網站）的所有github檔案皆使用自[oleeskild設定好的 Digital Garden 檔案](https://github.com/oleeskild/digitalgarden)，感謝每一位網路大神無私奉獻 🙏。   
>     <br>
> 3. 最後，本人完全沒有任何網頁架設和程式設計的底子，若有任何錯誤（或者bug）歡迎來信指正，我們一起研究、一起學習！以下是我的聯絡信箱：   <br>
>    📪 `tree10zi23@gmail.com`


## ⚒️ 事前準備




> [!tip] 架站之前請先準備以下幾項工具：
>  - [ ] 一個 Obsidian 儲存庫（Vault）[^2]






https://wanderloots.xyz/
- https://github.com/jackyzha0/quartz?tab=readme-ov-file
- https://quartz.jzhao.xyz/
- https://github.com/oleeskild/obsidian-digital-garden
- https://app.netlify.com/teams/litree318/sites `my_metlify`
- https://github.com/LiTree318?tab=repositories `my_github`


### 我的求救訊息

> [!tip]- ~~卡關~~ 解決 `patch20250505` 
> 解決了，==感謝陳建男（叔叔）和邱佳昇支援==！！！><
> 最近在研究Obsidian匯出網頁的功能，找到 #DigitalGarden 的介紹（連結一）。
> 自己實測了幾天，發現無論如何還是無法成功發佈網站。看有沒有一樣有在用Obsidian 結合 Github 和 Netlify 管理網站的朋友，知道我該怎麼解決問題。
> 1️⃣ 連結二是我自己上傳的檔案，預計要將這些文件發佈在網頁上。
> 2️⃣ 我參考了幾個用相似方式製作網站的案例（連結三、連結四），我發現在我的資料庫裡面，缺少 json 檔和一些設定檔案；我估算是因為只上傳Markdown檔，所以Netlify 無法辨認，從而使得網頁失敗（連接五）
> 3️⃣ 連結六我把包含obsidian預設檔的所有檔案放在同一個資料庫底下，並另外申請一個網域做測試（連結七）；但得到的結果與連結五相同，也就是說 Netlify 收到檔案，但無法匯出成網頁格式。
> 4️⃣ 我現在不清楚應該怎麼做，是需要重新撰寫一份包含HTML、CSS和Json的檔案，是哪個環節出錯？
> ---
> 以上，再請問板上朋友有緣、有空支援（之後可以請吃一頓飯作為酬勞，或者看有什麼我可以報答的部分）
> 連結一： Digital Garden網站： https://wanderloots.xyz/
> 連結二：測試A連結： https://github.com/LiTree318/sadtreeqaq318zzz
> 連結三：Peter's 2nd Brain： https://peteryuen.netlify.app/
> 連結四：RW Tech Wiki： https://rwtechwiki.github.io/
> 連結五：基於測試A（連結二）資料庫生成的網頁： https://sadtreeqaq318zzz.netlify.app/
> 連結六：測試B連結： https://github.com/LiTree318/happytree318
> 連結七：基於測試B（連結六）資料庫生成的網頁： https://happytree318.netlify.app/


[[publish/index\|index]]

[^1]: 這部份特別感謝[邱佳昇支援](https://www.facebook.com/share/p/16YThn4q9h/)，讓我可以按圖索驥找出自己的bugs（2025年5月5日）。
[^2]: 由於我是使用全英文介面的 Obisidn（為了用快捷搜尋），因此之後本分文件所有用到的vault會統一用「儲存庫」來翻譯（這也是官方中文給定的譯名）。