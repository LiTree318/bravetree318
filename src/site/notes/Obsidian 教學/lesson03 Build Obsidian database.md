---
{"dg-publish":true,"dg-permalink":"2025-06-27-obsidian-03","permalink":"/2025-06-27-obsidian-03/","title":"L3 2025-06-27 建立 Obsidian 資料庫","metatags":{"og:title":"2025-06-27 建立 Obsidian 資料庫","og:image":"https://github.com/LiTree318/bravetree318/blob/30d06f8c84f5e1a799df01adf873ad965dabe42a/src/site/img/user/obsidian%20%E6%95%99%E5%AD%B8/ob%E4%BA%A4%E6%B5%81%E6%BA%96%E5%82%99/%E6%8A%95%E5%BD%B1%E7%89%875-06-01-25_08-32-52-831.png","description":"2025-06-27 建立 Obsidian 資料庫：筆記屬性與YAML／介紹「Dataview」套件／Dataview + 標籤／設定筆記屬性／核心套件： Dataview／建立第一個資料庫"},"tags":["🪨自籌Obsidian工作坊","🎯學習歷程檔案"],"created":"2025-06-20T16:24:36.000+08:00","updated":"2025-06-24T06:03:54.237+08:00"}
---


> [!info]- 簡報
> [2025-06-27 Obsidian 資料庫｜Slides](https://hackmd.io/@tree10zi23/2025-06-27-obsidian-lesson-03#/)

　　
![投影片5-06-01-25_08-32-52-851.png](/img/user/Obsidian%20%E6%95%99%E5%AD%B8/ob%E4%BA%A4%E6%B5%81%E6%BA%96%E5%82%99/%E6%8A%95%E5%BD%B1%E7%89%875-06-01-25_08-32-52-851.png)



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

```markdown
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
> ```markdown
> ---
> title: "練習一：新增一份帶有特定屬性的文件"
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
> > 我的案例 👉 [[Obsidian 教學/lesson-03-材料/hw-obsidian-lesson-03\|我的工作流程]] 



> [!success] 我的工作流程視覺圖（made by Obsidian）
> ![我的工作流程視覺圖.png](/img/user/Obsidian%20%E6%95%99%E5%AD%B8/lesson-03-%E6%9D%90%E6%96%99/image/%E6%88%91%E7%9A%84%E5%B7%A5%E4%BD%9C%E6%B5%81%E7%A8%8B%E8%A6%96%E8%A6%BA%E5%9C%96.png)


有了上面的架構圖，資料庫至少會需要拆分成四種不同類型的筆記；同時這些個別的筆記都會有不同的屬性，以便於串聯資料來源和不同階段的筆記。



### 介紹 Dataview 套件

- 安裝套件 [Dataview](obsidian://show-plugin?id=dataview)


> [!info]- Dataview 是什麼？
> Dataview 是 Obsidian 的套件，它提供使用者快速檢閱儲存庫裡（vault）裡面的資料和文件，並能透過設定方式篩選、排序、和取用特定的資料與頁面。
> 
> 關於 Dataview 的詳細說明可以參考這個網址：[Obsidian Dataview](https://blacksmithgu.github.io/obsidian-dataview/)


Dataview 包含三種不同的呈現方式：table、list、task。最常使用的呈現方式是table 和 list（如下圖）。


如圖所示，上圖是 Dataview 程式語言和指令，下圖則是呈現出來的效果。從顯示畫面可以看出我們可以透過不同的指令和標籤來顯示特定的資料，這樣我們可以更快找到自己想要的檔案。資料庫分類的基準是依照我們在每一份文件設定的屬性（或者透過標籤）來進行分類，因此前面我們提到要先規劃好個人資料庫的資料架構還有邏輯，目的就是為了讓我們在後續建立檢索方式時，可以更清楚知道我們此時要檢索的資料是哪些資料。

關於 Dataview 詳細的用法，加在後面「機上操作」說明。

| Dataview 比較： TABLE（表格，右圖）和 LIST（清單，左圖） |
| :------------------------------------: |
|        ![TABLE and LIST.png](/img/user/Obsidian%20%E6%95%99%E5%AD%B8/lesson-03-%E6%9D%90%E6%96%99/image/TABLE%20and%20LIST.png)         |


---

## PART 2：機上操作

### 設定筆記屬性

![我的工作流程視覺圖.png](/img/user/Obsidian%20%E6%95%99%E5%AD%B8/lesson-03-%E6%9D%90%E6%96%99/image/%E6%88%91%E7%9A%84%E5%B7%A5%E4%BD%9C%E6%B5%81%E7%A8%8B%E8%A6%96%E8%A6%BA%E5%9C%96.png)

依照這張圖上的筆記類別，先來新增不同類型的筆記（請結合上週分享過的[[Obsidian 教學/lesson02 Basic skills of Obsidian#Templates（模板）\|模板套件]]）：

> [!example] 我的筆記清單
> 1. [[Obsidian 教學/lesson-03-材料/lesson03 Example01 Sources Template\|🏷️ 原始資料／資料來源]] 
> 2. [[Obsidian 教學/lesson-03-材料/lesson03 Example02 Note Template\|📝 摘錄內容／我的筆記]]
> 3. [[Obsidian 教學/lesson-03-材料/lesson03 Example03 Library view Template\|🗃️ 資料庫／知識地圖／圖書館]]
> 4. [[Obsidian 教學/lesson-03-材料/lesson03 Example04 Article Template\|📃 草稿／文章／成品]]
> 


### 設定 Dataview

#### 基礎使用方式：清單（list）

```markdown
LIST
tags + "日期：" +  date
FROM #自學
SORT file.mtime DESC
```
##### 解析與延伸
```markdown
LIST 
	# 表示用清單的方式顯示資料

tags + "日期：" +  date
	## tags 表示在每一筆清單資料中加上「tags」
	## 用 `+` 號來連結不同的屬性
	## 如果要再用輸入其他文字，需要用 "這邊是文字" 來表示。

FROM #自學
	## FROM 代表篩選條件，只能用 tags 篩選資料。
	## 如上所示，選擇「自學」之後就只會顯示「tags」中有「自學」的資料

SORT file.mtime DESC
	## SORT 是排序方法，分成：
	## ASC 順序排，由小到大，由舊到新；
	## DESC 倒序排，由大倒小，由新到舊。
	## SORT 的指令為： `SORT <條件> ASC/DESC`
		## 條件需要是「文件的屬性」
	## `file.mtime` 代表：文件最後修改時間。
	## 幾個常用的指令如下：
		## file.title 文件標題（筆劃）
		## file.ctime 文件創立時間
```
#### 基礎使用方式：表格（table）

```markdown=
TABLE
author as "作者",
date as "資料日期",
tags as "主題"
FROM #自學
SORT file.mtime DESC
```

##### 解析與延伸

```markdown
TABLE # 表示用表格的方式顯示資料
	## 不同欄位之間要用 "," 來區隔

author as "作者", 
	## 表示把資料中「author」提取呈現，
	## 用 AS "標題名稱" 可以自定欄位標題

date as "資料日期",
	## 表示把資料中「date」提取呈現，
	## 用 AS "標題名稱" 可以自定欄位標題

tags as "主題"
	## 表示把資料中「tags」提取呈現，
	## 用 AS "標題名稱" 可以自定欄位標題
FROM #自學
	## FROM 代表篩選條件，只能用 tags 篩選資料。
	## 如上所示，選擇「自學」之後就只會顯示「tags」中有「自學」的資料

SORT file.mtime DESC
	## SORT 是排序方法，分成：
	## ASC 順序排，由小到大，由舊到新；
	## DESC 倒序排，由大倒小，由新到舊。
	## SORT 的指令為： `SORT <條件> ASC/DESC`
		## 條件需要是「文件的屬性」
	## `file.mtime` 代表：文件最後修改時間。
	## 幾個常用的指令如下：
		## file.title 文件標題（筆劃）
		## file.ctime 文件創立時間
```
#### 進階用法

##### 設定複數條件檢閱：`WHERE`

```markdown
WHERE 
contains(type, "🏷️資料來源") and
!contains(file.name, "Template")
	## WHERE 是另外一種篩選條件的指令，指令為 contains(<屬性名稱>,"<指定條件>")
	## `contains` 表示：包含這個條件。
	## `!contains` 表示：不包含這個條件。
	## 超過一個條件需要輸入 and 來並列，例如：
		## WHERE
		## contains(屬性1,"條件1") AND
		## !contains(屬性2, "條件2")

```

##### 以特定文字呈現檔案連結： `link(file.link,<特定文字>)`

```
link(file.link, "<特定文字>")
```

##### 組裝文字： `<文字>+<文字>`
```
"<文字1>" + "<文字2>"
```


### 建立第一個資料庫


|   建構資料庫流程視覺圖   |
| :------------: |
| ![建構資料庫.png](/img/user/Obsidian%20%E6%95%99%E5%AD%B8/lesson-03-%E6%9D%90%E6%96%99/image/%E5%BB%BA%E6%A7%8B%E8%B3%87%E6%96%99%E5%BA%AB.png) |


## PART 3：問題與討論

> [!EXAMPLE] 研究問題
> - [ ] 建構資料庫的底層邏輯是什麼？主要處理的資料型態、產出成品的形態，以及處理的議題是什麼？
> - [ ] 除了透過標籤管理資料庫之外，還有哪些管理資料庫的方式？
> - [ ] 如何讓資料庫更便捷使用？
> - [ ] RECYCLE：再利用每次的資料與筆記？


> [!NOTE] 課後練習
> - [ ] 如何使用 `flatten` 和 `group` 指令？他的用途是什麼？
> - [ ] 是否有**動態**調整資料庫的方式？



[^2]: 參考資料：YAML，Wikipedia。https://zh.wikipedia.org/zh-tw/YAML