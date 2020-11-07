# arXivS API

🎉 欢迎使用 [arXivS API](www.arxivs.com/doc)，请按照以下规则访问。

## URL

`https://api.arxivs.com/papers/others?number=5&skip=0&sort=lastest&tag=all&resource=all`

## Required parameters

1. number ：
  - 说明：请求数据的数量。
  - 取值范围： `1 - 100`
  - 默认： `5`
2. skip ：
  - 说明：请求数据跳过的数量，用于下拉刷新加载。
  - 取值范围： `0 - 10000`
  - 默认： `0`
3. sort ：
  - 说明：请求数据排序方式。
  - 取值范围：
    - `lastest`: 按照最新排序。
    - `popular`: 按照最热排序。
    - `collection`: 用户收藏（仅小程序可以使用）。
  -默认： `lastest`
4. tag ：
  - 说明：请求数据的标签。
  - 取值范围：
    - `all`：所有下述标签。
    - `cs.AI`: Artificial Intelligence
    - `cs.CL`: Computation and Language
    - `cs.CV`: Computer Vision and Pattern Recognition
    - `cs.FL`: Formal Languages and Automata Theory
    - `cs.IR`: Information Retrieval
    - `cs.LG`: Learning
    - `cs.MA`: Multiagent Systems
    - `cs.NE`: Neural and Evolutionary Computing
    - `stat.ML`: Machine Learning
  - 默认： `all`
5. resource :
  - 说明：请求数据中包含资源。
  - 取值范围：
    - `all`：所有下述资源。
    - `github`: 带有 github 链接。
  - 默认： `all`

## Example

```Python
# Python
import requests

payload = {
	"number": 5,
	"skip": 0,
	"sort": "lastestPapers",
	"tag": "all",
	"resource": "all"
}

response = requests.get("https://api.arxivs.com/papers/others", params=payload)
print(response.json())
```
