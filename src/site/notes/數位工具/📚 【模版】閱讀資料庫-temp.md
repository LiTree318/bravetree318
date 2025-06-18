---
{"dg-publish":true,"permalink":"/數位工具/📚 【模版】閱讀資料庫-temp/","title":"📚 【模版】閱讀資料庫-temp","noteIcon":"3","created":"2025-05-08T13:23:53.000+08:00","updated":"2025-06-18T15:37:32.634+08:00"}
---



### 資料庫指令


> [!NOTE]- 📀 指令
> ```
> TABLE without id
> 	file.link as "Quate",
>   row.page as "Cite-pages",
> 	file.inlink as "Mentions",
>   length(file.inlinks) as "Count of Mentions",
>  	literature as "References/Literatures"
> FROM #reading_notes AND #literatures
> where !contains(file.name, "temp")
> SORT "last-modified" ASC
> ```


---

### 筆記頁面套件


> [!NOTE]- 📀 指令 
> 詳細說明[[後續會再補充\|後續會再補充]]。 #📝數位工具交流beta #Reading_Notes #Books 
> 
> ```
> <%* 
> let book = await tp.system.prompt("請輸入書名");
> %>---
> title: "<% book %> - Quotations List" 
>  book: "<% book %>" 
> c.reate-date: "<% tp.date.now('YYYY-MM-DD HH:mm') %>"
> ---
> 
> %% 
> tags:: #Books 
> type:: "🔖 table of content"
> %%
> 
> // 這邊輸入上面資料庫的指令//
> 
> ## my-review
> ```
