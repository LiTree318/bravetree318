---
{"title":"📚 閱讀資料庫（模版）","create-date":"2025-05-08 10:56","dg-publish":true,"permalink":"/ignore/00. template/📚 【模版】閱讀資料庫-temp/","dgPassFrontmatter":true,"created":"2025-05-08T12:19:19.604+08:00","updated":"2025-05-08T13:00:35.826+08:00"}
---


	tags:: #Books  #literature #📝數位工具交流beta 
	type:: "🔖 table of content"     





## 資料庫指令


> [!NOTE]- 📀 指令
> ```markdown
>  | Quate                                                                                                    | Cite-pages | Mentions | Count of Mentions | References/Literatures |
> | -------------------------------------------------------------------------------------------------------- | ---------- | -------- | ----------------- | ---------------------- |
> | [[閱讀/人魚紀/「日常」的滾輪，是一種伏筆嗎？暗示著這一切努力之後會再次回歸日常，只會剩下一搓小小的怪奇.md\|「日常」的滾輪，是一種伏筆嗎？暗示著這一切努力之後會再次回歸日常，只會剩下一搓小小的怪奇]] | \-         | \-       | 0                 | 人魚紀                    |
> | [[閱讀/人魚紀/反覆地練習才能塑造「身體」.md\|反覆地練習才能塑造「身體」]]                                                               | \-         | \-       | 0                 | 人魚紀                    |
> | [[閱讀/人魚紀/另一種排除是「身體」的排除，東尼是「對的身體」.md\|另一種排除是「身體」的排除，東尼是「對的身體」]]                                           | \-         | \-       | 0                 | 人魚紀                    |
> | [[閱讀/人魚紀/國標舞.md\|國標舞]]                                                                                   | \-         | \-       | 0                 | 人魚紀                    |
> | [[閱讀/人魚紀/基本功夫與表面工夫.md\|基本功夫與表面工夫]]                                                                       | \-         | \-       | 0                 | 人魚紀                    |
> 
{ .block-language-dataview}


---

### 筆記頁面套件


> [!NOTE]- 📀 指令 
> 詳細說明[[後續會再補充]]。 #📝數位工具交流beta #Reading_Notes #Books 
> 
> ```markdown
>     <%* 
> let book = await tp.system.prompt("請輸入書名");
> %>---
> title: "<% book %> - Quotations List" 
>  book: "<% book %>" 
> c.reate-date: "<% tp.date.now('YYYY-MM-DD HH:mm') %>"
> location: "💻mac-air"
> ---
> 
> 
> 
>      | File | citation-pages | mentions | count-of-mentions | last-modified |
> | ---- | -------------- | -------- | ----------------- | ------------- |
> 
{ .block-language-dataview}
> 
> 
> 
> ## my-review
> ```
