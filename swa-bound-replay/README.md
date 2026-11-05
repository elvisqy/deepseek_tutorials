# SWA Replay 流程

以动态、可交互的方式说明 DeepSeek V4.1-Flash 的 SWA Replay 执行流程，重点回答以下问题：

- Replay 开启时，Encoder 与 Decoder 分别处理哪些 token 行。
- 长历史 KV 命中后，为什么还需要重放命中前缀末尾的窗口。
- 各层如何恢复自己的 SWA Cache，以及最终活动窗口如何滚动。
- Replay 关闭时，同一前向批次中 L0-L39 为什么具有相同的 token 行集合。
- 长历史 Cache 与 SWA Cache 命中边界不同时，本轮需要补算哪些 token。

## 阅读方式

- 在线阅读：<https://elvisqy.github.io/deepseek_tutorials/swa-bound-replay/>
- 查看 HTML 文件：[`index.html`](./index.html)
- 离线阅读：下载 `index.html`，使用浏览器打开即可。字体、样式和图表已包含在单个 HTML 文件中。

GitHub 仓库文件页面会展示 HTML 源码；如果需要直接阅读，请使用 GitHub Pages 或下载到本地打开。

## 文件结构

```text
swa-bound-replay/
├── index.html
└── README.md
```
