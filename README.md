# 财经资讯解读

`laogu-news`

财经资讯解读 skill：输入一篇财经新闻/研报/公告，输出结构化中文解读。

## 解读框架

按 `SKILL.md` 的 Workflow 执行：事实提取 → 影响链条 → 多空判断 → 关联标的 → 历史类比 → 跟踪清单。

## 输入示例

- 新闻链接或全文："央行宣布降准 0.5 个百分点"
- 研报观点："某券商上调锂行业评级至超配"
- 公告："XX 公司发布定增预案，募资 20 亿扩产"
- 可附加关注方向："我持有新能源仓位，重点看对锂电的影响"

## 输出示例（结构）

- 事件摘要：发生了什么（纯事实，3-5 句）
- 影响链条：直接影响 → 传导路径 → 二级影响
- 多空判断：短期/中期，偏多/偏空/中性 + 逻辑与假设
- 关联标的：A股公司代码 + 关联逻辑
- 历史类比：相似事件 + 当时市场反应（仅供参考）
- 后续跟踪点：要盯的数据/事件/时间点

## 说明

- 事实与推断严格区分，推断标注"推测"
- 只讲逻辑，不做买卖推荐

---
## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。

## 一键安装

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-news`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-news.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-news/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-news/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
