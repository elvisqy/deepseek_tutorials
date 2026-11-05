# DeepSeek-V4.1-Flash 结构分析报告

DeepSeek-V4.1-Flash 的模型结构分析 HTML 归档。

报告主要涵盖：

- 模型定位、官方核心指标与目标场景。
- CED 架构的参数、层分布与层类型汇总。
- A 类 SWA MoE 层、B 类 CSA2-r2 共享层、C 类 Decoder 层，以及 Engram 和 DSpark 草稿层。
- 每 Token KV Cache 占用量与参数量分项估算。
- CED、CSA2、FP4 KV、Engram、Single-Pass mHC 与 DSpark 的结构收益和设计取舍。

## 阅读方式

- 在线阅读：<https://elvisqy.github.io/deepseek_tutorials/model-analysis/DeepSeek-V4.1-Flash/>
- 查看 HTML 文件：[`index.html`](./index.html)
- 离线阅读：下载 `index.html`，使用浏览器打开即可。

GitHub 仓库文件页面会展示 HTML 源码；如果需要直接阅读，请使用 GitHub Pages 或下载到本地打开。

## 文件结构

```text
model-analysis/
└── DeepSeek-V4.1-Flash/
    ├── index.html
    └── README.md
```
