---
title: 🧭 Index
tags:
  - dashboard
  - index
created: <% tp.date.now("YYYY-MM-DD") %>
updted:
---
# 🧭 Vault Index
Welcome to the main entry point. Use this dashboard to navigate the Notes, How-To guides, README references, and daily logs.

---
# 📄 Reference Notes
```dataview
TABLE file.name as "Topic", file.mtime as "Last Updated"
FROM "content/knowledgebase"
WHERE contains(type, "readme")
SORT file.mtime desc
```


## 📚 Atom Notes
```dataview
TABLE file.name as "Note", file.mtime as "Last Modified"
FROM "content/knowledgebase/atoms"
WHERE contains(type, "atom")
SORT file.mtime desc
```


# 🛠️ How-To Guides
```dataview
TABLE file.name as "Note", file.mtime as "Last Modified"
FROM "content/knowledgebase/how_to"
WHERE contains(type, "how_to")
SORT file.mtime desc
```


# 📅 Daily Logs
```dataview
TABLE file.name as "Log", created
FROM "content/knowledgebase/journal_logs"
WHERE contains(type, "daily")
SORT file.mtime desc
```

