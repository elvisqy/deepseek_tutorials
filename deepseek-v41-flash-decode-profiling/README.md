# DeepSeek V4.1 Flash Decode 算子图与优化推导

用一轮 Ascend NPU 0 的 Decode 采样，展示输入准备、目标模型 40 层和 DSpark 草稿图 3 层。点击算子可以查看实测耗时、执行流、输入输出形状和对应用途。

「优化点与推导」从 L24 的 Lightning Indexer 开始，演示怎样从原始时间线找到优化线索，再结合源码和 PR 确认改法。报告同时列出七组优化、对应算子和验证方法。PR 基准数据采用各自的测试条件。

## 阅读方式

- [在线阅读](https://elvisqy.github.io/deepseek_tutorials/deepseek-v41-flash-decode-profiling/)
- [查看 HTML 文件](./index.html)
- 离线阅读时，下载 `index.html` 后用浏览器打开。报告的数据、样式和交互均包含在 HTML 中。

## 文件结构

```text
deepseek-v41-flash-decode-profiling/
├── index.html
└── README.md
```
