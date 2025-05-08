---
{"dg-publish":true,"title":"📑 【模版】參考資料引用-temp","tags":["📝數位工具交流beta","self_learing"],"permalink":"/ignore/00. template/📑 【模版】參考資料引用-temp/","dgPassFrontmatter":true,"created":"2025-05-08T12:23:21.556+08:00","updated":"2025-05-08T12:28:34.834+08:00"}
---


# 📑 【模版】參考資料引用

請將以下的code複製到md上。

> [!NOTE] 備註
> 需要先安裝 Templater、並開啟相關[[設定\|設定]]。

```markdown
<%* 
let literature = await tp.system.prompt("請輸入資料標題");
let author = await tp.system.prompt("請輸入作者／編者／譯者");
let year = await tp.system.prompt("請輸入資料年份（日期）");
let reference = await tp.system.prompt("【選填】請輸入資料來源");
let volume = await tp.system.prompt("【選填】請輸入期刊卷（volume）");
let issue = await tp.system.prompt("【選填】請輸入期刊期（issue）");
let url = await tp.system.prompt("【選填】請輸入資料網址");
let pages = await tp.system.prompt("請輸入頁數範圍");

%>---
title: "<% tp.file.title %>"
tag: #literatures #reading_notes #📝數位工具交流beta 
annotation-target: 
c-date:: "<% tp.date.now('YYYY-MM-DD HH:mm') %>"

---

%% 
	author:: "<% author %>"
	year:: "<% year %>"
	literature:: "<% literature %>"
	reference:: "<% reference %>"
	volume:: "<% volume %>"
	issue:: "<% issue %>"
	url:: "<% url %>"
	pages:: "<% pages %>" 
%%




# <% tp.file.title %>




## Quotations

tp.file.cursor()


> [!QUOTE] Pages  <% pages %>
> 摘要
> 摘要


---

# My Review



> [!NOTE] 
> Contents

---
## 🔍 研究背景

> [!warning] 注意
> 1. 真實世界的經驗現象
> 2. 理論對於該現象的討論

### 🖼️ 現象

### 🧪 理論


---
## ✍️ 作者的提問／研究問題

> 理論無法解釋的現象，為什麼無法解釋、造成什麼盲點？限制哪些討論？


### 🎯 研究假設與研究規劃
> 假設與說故事


### 🔢 資料與分析
> 資料取得、整理和分析架構


### ✅ 研究結果與討論
> 結果與解釋、結論與貢獻、限制與不足


---
## ❓提問


```