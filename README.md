# 实时新闻 Realtime News

获取实时新闻热榜：微博热搜、百度热榜、知乎热榜、今日头条热榜、36氪热榜、腾讯新闻热榜、B站热榜、澎湃新闻热榜、虎扑步行街热榜、抖音热榜、IT资讯热榜、虎嗅热榜、百度贴吧热榜、稀土掘金热榜。
Obtain real-time news trending lists: Weibo Hot Search, Baidu Hot List, Zhihu Hot List, Jinri Toutiao Hot List, 36Kr Hot List, Tencent News Hot List, Bilibili Hot List, The Paper Hot List, Hupu Walking Street Hot List, TikTok Hot List, IT News Hot List, Huoxiu Hot List, Baidu Tieba Hot List, Juejin Hot List.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| weibo_news | 实时数据/微博热搜 |
| baidu_news | 实时数据/百度热榜 |
| zhihu_news | 实时数据/知乎热榜 |
| toutiao_news | 实时数据/今日头条热榜 |
| 36ke_news | 实时数据/36氪热榜 |
| tx_news | 实时数据/腾讯新闻热榜 |
| bli_news | 实时数据/B站热榜 |
| sougou_news | 实时数据/搜狗热榜 |
| sougou_a_news | 实时数据/搜狗热榜A |
| pengpai_news | 实时数据/澎湃新闻热榜 |
| hupu_news | 实时数据/虎扑步行街热榜 |
| hupu_a_news | 实时数据/虎扑步行街热榜A |
| douyin_news | 实时数据/抖音热榜 |
| it_news | 实时数据/IT资讯热榜 |
| huxiu_news | 实时数据/虎嗅热榜 |
| baidu_tieba_news | 实时数据/百度贴吧热榜 |
| xitu_news | 实时数据/稀土掘金热榜 |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1804087353852938](https://mcp.xiaobenyang.com/inspector/1804087353852938)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1804087353852938](https://mcp.xiaobenyang.com/inspector/1804087353852938)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "实时新闻": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1804087353852938/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "实时新闻": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1804087353852938/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "实时新闻": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1804087353852938",
          },
          "transport": "stdio"
        }
      }
}

```
