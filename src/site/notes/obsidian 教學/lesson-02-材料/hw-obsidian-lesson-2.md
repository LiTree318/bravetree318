---
{"dg-publish":true,"permalink":"/obsidian 教學/lesson-02-材料/hw-obsidian-lesson-2/","title":"HW-2025-06-20 （作業01） 用套件檢視資料","tags":["🪨自籌Obsidian工作坊","🎯學習歷程檔案"],"noteIcon":"3","created":"2025-06-17T22:54:37.974+08:00","updated":"2025-06-20T12:08:46.756+08:00"}
---


### 清單（List）檢視

```

	```#dataview
	LIST
	"　　" + replace(string(tags), ", ", " #") + "　　進度：
	" + file.進程
	```
	
```

---


### 表格（Table）檢視

```
	```#dataview
	TABLE
	replace(string(tags), ", ", " #") as "標籤",
	file.進程 as "進度"
	```
```
