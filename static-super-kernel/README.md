# Static Kernel 与 Super Kernel

以动态、可交互的方式说明 DeepSeek V4.1-Flash 在 vLLM Ascend 图编译路径中的 Static Kernel 与 Super Kernel 优化。

页面重点覆盖：

- ACLGraph、npugraph_ex、Static Kernel 与 Super Kernel 在 Decode 执行栈中的分工。
- Static Kernel 如何把固定 shape 的合格算子编译成专用二进制，并在运行时命中对应 bucket。
- MTP、capture size 与运行时 token 对齐如何影响 Static Kernel 的覆盖范围。
- Super Kernel 如何在静态二进制之上组织连续合格子图，减少 kernel 任务碎片。
- 40 层主干中哪些结构更适合静态化与融合，以及 P/D 两端的覆盖差异。
- 启动日志、Profiling 指标、验收清单和建议的首次 A/B 方法。

本页解释机制、适用条件与收益来源，不把结构性优化空间当作 A3 实测性能结论。

## 阅读方式

- 在线阅读：<https://elvisqy.github.io/deepseek_tutorials/static-super-kernel/>
- 查看 HTML 文件：[`index.html`](./index.html)
- 离线阅读：下载 `index.html`，使用浏览器打开即可。

GitHub 仓库文件页面会展示 HTML 源码；如果需要直接阅读，请使用 GitHub Pages 或下载到本地打开。

## 文件结构

```text
static-super-kernel/
├── index.html
└── README.md
```
