---
{"dg-publish":true,"title":"📑 【模版】參考資料引用-temp","tags":["📝數位工具交流beta","self_learing"],"permalink":"/數位工具/📑 【模版】參考資料引用-temp/","dgPassFrontmatter":true,"created":"2025-05-08T13:23:53.000+08:00","updated":"2025-05-10T21:59:48.597+08:00"}
---



請將以下的code複製到md上。

> [!NOTE] 備註
> 需要先安裝 Templater、並開啟相關[[設定\|設定]]。

### 指令



> [!NOTE]- 📀 Code
> 
> ```
> 	<%* 
> 	let literature = await tp.system.prompt("請輸入資料標題");
> 	let author = await tp.system.prompt("請輸入作者／編者／譯者");
> 	let year = await tp.system.prompt("請輸入資料年份（日期）");
> 	let reference = await tp.system.prompt("【選填】請輸入資料來源");
> 	let volume = await tp.system.prompt("【選填】請輸入期刊卷（volume）");
> 	let issue = await tp.system.prompt("【選填】請輸入期刊期（issue）");
> 	let url = await tp.system.prompt("【選填】請輸入資料網址");
> 	let pages = await tp.system.prompt("請輸入頁數範圍");
> 	%>---
> 	title: "<% tp.file.title %>"
> 	tag: #literatures #reading_notes #📝數位工具交流beta 
> 	annotation-target: 
> 	c-date:: "<% tp.date.now('YYYY-MM-DD HH:mm') %>"
> 	---
> 	%% 
> 		author:: "<% author %>"
> 		year:: "<% year %>"
> 		literature:: "<% literature %>"
> 		reference:: "<% reference %>"
> 		volume:: "<% volume %>"
> 		issue:: "<% issue %>"
> 		url:: "<% url %>"
> 		pages:: "<% pages %>" 
> 	%%
> # <% tp.file.title %>
> 
> 
> ## Quotations
> 
> [!QUOTE] Pages  <% pages %>
> 摘要
> 
> ---
> 
> # My Review
> 
> 
> ## 🔍 研究背景
> ---
> ## ✍️ 作者的提問／研究問題
> ---
> ## ❓提問
> 
> 
> ```