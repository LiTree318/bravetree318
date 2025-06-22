---
{"dg-publish":true,"dg-permalink":"2025-06-27-obsidian-03","permalink":"/2025-06-27-obsidian-03/","title":"L3 2025-06-27 建立 Obsidian 資料庫","metatags":{"og:title":"2025-06-27 建立 Obsidian 資料庫","og:image":"https://github.com/LiTree318/bravetree318/blob/30d06f8c84f5e1a799df01adf873ad965dabe42a/src/site/img/user/obsidian%20%E6%95%99%E5%AD%B8/ob%E4%BA%A4%E6%B5%81%E6%BA%96%E5%82%99/%E6%8A%95%E5%BD%B1%E7%89%875-06-01-25_08-32-52-831.png","description":"2025-06-27 建立 Obsidian 資料庫：筆記屬性與YAML／介紹「Dataview」套件／DV + 標籤／設定筆記屬性／核心套件： Dataview／建立第一個資料庫"},"tags":["🪨自籌Obsidian工作坊","🎯學習歷程檔案"],"noteIcon":"3","created":"2025-06-20T16:07:09.100+08:00","updated":"2025-06-22T13:27:42.723+08:00"}
---


> [!info]- 簡報
> ### [[obsidian 教學/lesson-03-材料/obsidian-dataabase-slides\|第三堂課課程簡報]]

　　
![投影片5-06-01-25_08-32-52-851.png](/img/user/obsidian%20%E6%95%99%E5%AD%B8/ob%E4%BA%A4%E6%B5%81%E6%BA%96%E5%82%99/%E6%8A%95%E5%BD%B1%E7%89%875-06-01-25_08-32-52-851.png)



## PART 1： 概念說明

### 筆記屬性

在 Markdown 語言中，每一份文件的==第一行==可以輸入 `---` 來形成 `YAML` 區域。


> [!NOTE] 👉 什麼是 YAML 
> YAML 是「 *Yet Another Markup Language*」（仍是另一種標記語言）的簡稱[^2]。同樣是一種程式語言，可以讓文件具備系統化的資料屬性。
> 
> 在我們的使用上，YAML 可以賦予筆記各式各樣的屬性，從而讓我們管理筆記和資料庫能變得更容易。
> 
> YAML的官網： https://yaml.org/


yaml 區域要求在文件的第一行開始：輸入 `---`可以開啟yaml 區域（如下）：

```
---
title: #在 title 輸入標題，可以設定文件的標題
tags:  #tags輸入標籤，可以設定文件的標籤
- 標籤一
- 標籤二
date: #在 date 輸入日期，可以設定文件的日期。預設格式為：年年年年-月月-日日；例如：2025-06-21
author: #在 author 輸入人名，可以設定文件的作者
---

```
所有YAML內容結束後，再以 `---` 收尾，夾住的內容就是這份文件的屬性。


> [!example] 練習一：新增一份帶有特定屬性的文件
> ```
> ---
> title: 練習一：新增一份帶有特定屬性的文件
> tags: 
> - 練習一
> - YAML
> - 自學筆記
> - 程式語言
> date: 2025-06-21
> author: TreeZi
> ---
> ```
> 
> 開啟新的筆記，將上述的內容複製貼到新筆記上。
> 
> 🔔 注意：請記得貼在**文件第一行**。
> 👉 顯示行號：`選單` → `編輯器` → `顯示行號` ✅

除了上述幾個既定的屬性外，YAML 語言可以新增自定的屬性，而我們可以用這些屬性來輔助我們管理筆記和資料庫。

### 建置資料庫
應用 yaml 語言之前，我們需要先釐清你想要 ==怎麼管理資料==；因此我們需要先規劃好==資料庫的邏輯==，哪些筆記要具備哪些屬性，而我們要怎麼使用這些筆記。

說起來有點抽象，讓我們直接來練習。

> [!example] 練習二：建置資料結構圖
> 1. 條列自己的工作流程（如果是寫作，條列自己的寫作流程），
> 2. 思考每個工作流程需要什麼樣類型的筆記。
> 3. 條列這些筆記需要具備哪些屬性。
> 4. 將上述的事項畫成「流程圖」。
>    
> ---
> > 我的案例 👉 [[obsidian 教學/lesson-03-材料/hw-obsidian-lesson-01\|我的工作流程]] 











👉 筆記屬性與YAML[^1]

👉 介紹「Dataview」套件

👉 DV + 標籤
　　

／／機上操作

⬇️ 設定筆記屬性

⬇️ 核心套件： Dataview

⬇️ 建立第一個資料庫



[^1]: https://yaml.org/spec/1.2.2/
[^2]: 參考資料：YAML，Wikipedia。https://zh.wikipedia.org/zh-tw/YAML