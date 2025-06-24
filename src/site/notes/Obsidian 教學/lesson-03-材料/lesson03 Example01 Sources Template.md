---
{"dg-publish":true,"dg-permalink":"lesson03_example01","permalink":"/lesson03_example01/","title":"模板01：🏷️ 原始資料／資料來源","tags":["🪨自籌Obsidian工作坊"],"created":"2025-06-22T14:53:38.705+08:00","updated":"2025-06-22T16:36:58.132+08:00"}
---



```markdown
---
title: "{{title}}"
type:
  - 🏷️資料來源
tags: 
create-date: "{{date: YYYY-MM-DD-DDDD}}"
---


> [!info]+ ⚙️ 額外屬性
> ⌨ 輸入額外屬性
> 	```	
> 		source:: 
> 		date::
> 		author::
> 		link:: 
> 		note::
> 	```
> > [!example] 額外屬性說明
> > 	```
> > 	// source 資料來源：網站／書籍／新聞等：
> > 		如果是網站：放上網站平台名稱（例如：CNN、Youtube）
> > 		如果是書籍中的文章：放上書籍名稱（例如：花蓮學研討會論文集）
> > 		如果是新聞：放上新聞媒體名稱（例如：自由時報、聯合報）
> > 	// date 放上資料的建置日期。
> > 	// author 放上資料的作者。
> > 	// link 放上資料來源的網址或連結（如果有的話）。
> > 	// note 放上其他需要註解該資料的備註。
> > 	```





## 🗃️ 摘錄清單

	```/dataview
	LIST 
	replace(
		"#" + 
		replace(
			string(tags),
			", ", 
			 " #"), 
		 "##", 
		 "#")  +
	" 日期：" +
	date
	
	where 
	contains(title, "{{title}}") and
	contains(type, "🏷️資料來源") and
	!contains(file.name, "Template")
	SORT file.mtime DESC

	```


## ✍️ 我的筆記


```


