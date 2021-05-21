# JSON Formatter

An alfred workfow to formatter strings to beautiful JSON to you clipboard.

### Usage
1. Default `Ctrl + Alt + J` to formatter your clipboard content to standard JSON.
2. Active Alfred and enter default keyword `json`, paste your content, done.

### Customize

The core python script in the workflow looks like:

```python
import sys
import json

query = sys.argv[1]
print(json.dumps(json.loads(query), ensure_ascii=False, encoding='UTF-8', sort_keys=True, indent=4, separators=(',', ': ')))
```

If you are familiar with python, edit the params of `json.dumps()` to custom json format.
