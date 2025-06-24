---
{"dg-publish":true,"permalink":"/ignore/00. template/🗃️ Note box(temp)/","title":"<% tp.file.title %>","tags":["<%* const tags_list = [\"🗃️資料庫\"","\"文史資料\"","\"新聞報導\"","\"統計數據\"","\"政策報告\"","\"研究論文\"","\"書籍作品\"","\"影音媒材\"","\"自學應用\"] let tags = await tp.system.suggester(tags_list","tags_list","true","\"輸入相關主題\"","5) %> - <% tags %>"],"created":"2025-05-29T20:41:02.417+08:00","updated":"2025-06-25T01:50:37.667+08:00"}
---



# 🗃️ <% tp.file.title %>



> [!example] <% tp.file.title %>
> - URL: [<% tp.file.title %>](<% source %>)



> [!NOTE] 說明備註
> <% note %>


