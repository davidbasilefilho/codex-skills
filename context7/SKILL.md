---
name: context7
description: Retrieve current library, framework, and component documentation through Context7. Use for API lookup, code examples, usage verification, or facts likely newer than training data.
---

# Context7

Use Context7 instead of memory for current library docs. Basic access needs no API key but is rate-limited.

## Workflow

1. Find library ID:

```bash
curl -s "https://context7.com/api/v2/libs/search?libraryName=LIBRARY_NAME&query=TOPIC" | jq '.results[0]'
```

Required: `libraryName`, relevance-ranking `query`. Result includes `id`, `title`, `description`, `totalSnippets`. Inspect more results if first match is wrong.

2. Fetch focused docs:

```bash
curl -s "https://context7.com/api/v2/context?libraryId=LIBRARY_ID&query=TOPIC&type=txt"
```

Required: search-result `libraryId`, specific `query`. `type` defaults to `json`; prefer `txt` for reading. URL-encode spaces with `+` or `%20`. Use `jq` for JSON filtering.

Example:

```bash
curl -s "https://context7.com/api/v2/libs/search?libraryName=react&query=hooks" | jq '.results[0].id'
curl -s "https://context7.com/api/v2/context?libraryId=/websites/react_dev_reference&query=useState&type=txt"
```
