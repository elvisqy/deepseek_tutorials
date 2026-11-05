# DeepSeek Tutorials

DeepSeek 模型运行机制与推理优化的可视化教程集合。

## 教程

- [SWA Replay 流程](./swa-bound-replay/)：以动态流程说明 DeepSeek V4.1-Flash 在 Replay 开启和关闭时的窗口计算、缓存命中、逐层 SWA 恢复以及双缓存命中边界。
- [Static Kernel 与 Super Kernel](./static-super-kernel/)：从 ACLGraph、npugraph_ex、固定 shape 与连续子图融合出发，说明两类 kernel 优化的执行过程、适用边界、验证方式与 A/B 观测方法。
- [DeepSeek-V4.1-Flash 结构分析报告](./model-analysis/DeepSeek-V4.1-Flash/)：梳理官方模型定位、CED 40 层结构、单层算子、KV Cache 与参数量，以及 CSA2、FP4 KV、Engram、Single-Pass mHC 和 DSpark 等结构机制。

## 阅读方式

每个教程都提供自包含的 `index.html`。字体、样式和交互逻辑已经内嵌，下载后可以直接使用浏览器打开，不依赖额外资源文件。

## 目录约定

```text
deepseek_tutorials/
└── <tutorial-name>/
    ├── index.html
    └── README.md
```
