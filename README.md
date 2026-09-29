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
## English

**laogu-news — Financial news interpreter.** Paste a news article, research note or filing; get a structured Chinese readout: event summary, impact chain, bullish/bearish judgment. Install: `npx skills add laogu-caibao/laogu-news`.

## FAQ

**Q：laogu-news 有什么用？**
适合的场景：看到一条财经新闻/公告/研报，想知道它到底说了什么、影响链条是什么、偏多还是偏空。

**Q：数据可靠吗？会荐股吗？**
数字必须来自可核验的公开来源（上市公司公告、交易所公开数据、公开网页），取不到就标「未核验」，绝不编造；只做结构化整理与解读，不构成投资建议。

**Q：怎么安装？支持哪些 AI 平台？**
```bash
npx skills add laogu-caibao/laogu-news
```
平台中立 Markdown，Claude Code、Codex、豆包智能体、Workbuddy、扣子 Coze、Trae 等环境均可用；数据能力可用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)（`uvx laogu-mcp`）一次装齐。更多 skill 见[老谷拆财报组织主页](https://github.com/laogu-caibao)。
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

```bash
npx skills add laogu-caibao/laogu-news
```

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
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-news/`（项目级用 `.trae/skills/laogu-news/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
