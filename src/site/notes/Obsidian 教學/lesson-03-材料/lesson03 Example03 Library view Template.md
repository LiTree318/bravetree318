---
{"dg-publish":true,"dg-permalink":"lesson03_example03","permalink":"/lesson03_example03/","title":"模板03：🗃️ 資料庫／知識地圖／圖書館","tags":["🪨自籌Obsidian工作坊"],"created":"2025-06-22T15:34:03.000+08:00","updated":"2025-06-22T16:37:22.000+08:00"}
---


```markdown

---
title: "{{title}}"
type:
  - 🗃️資料庫
tags: 
create-date: "{{date: YYYY-MM-DD-DDDD}}"
---


## 檢視所有原始資料／ `🏷️資料來源`


	```/dataview
	TABLE WITHOUT ID
	
	link(file.link, title) as "資料標題",
	author as "作者",
	date as "資料時間",
	source as "資料來源",
	replace(
		"#" + replace(
			string(tags),
			", ",
			" #"),
		 "##",
		 "#") as "主題"
	
	where 
		contains(type, "🏷️資料來源") and
		!contains(file.name, "Template")
	
	SORT file.mtime DESC
	```

---

> [!tip]- 製作簡易的「參考資料清冊」
> 	```/dataview
> 	LIST WITHOUT ID
> 	
> 	choice(author = "",
> 		title + "（" +
> 		date + "），《"+
> 		source + "》。"+
> 		choice( link = "",
> 			"",
> 			"網址：" + link + "。 "),
> 		author + "（" +
> 		date + "），〈" +
> 		title + "〉，《" +
> 		source + "》。" +
> 		choice( link = "",
> 			"",
> 			"網址：" + link + "。 " ))
> 	
> 	where
> 		contains(type, "🏷️資料來源") and
> 		!contains(file.name, "Template")
> 	```


## 檢視所有❝引用內容❞／ `📝我的筆記`


	```/dataview
	TABLE WITHOUT ID
	quotation as "引用內容",
	note + "（" + link(file.link,
		choice(author="",
			source + "，" + "date" ,
			author + "，" + "date")) +"）" as "我的筆記",
	replace(
		"#" + replace(
			string(tags),
			", ",
			" #"),
		 "##",
		 "#") as "主題"
	
	where 
		contains(type, "📝我的筆記") and
		!contains(file.name, "Template")
	
	SORT file.mtime DESC
	```



```



