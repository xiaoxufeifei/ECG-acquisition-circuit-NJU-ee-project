# GitHub 发布文案

## 项目题目

**中文：** 心电信号模拟前端：从电路设计到实物验证

**英文：** ECG Analog Front End: From Circuit Design to Hardware Validation

**建议仓库名：** `ecg-analog-front-end`（名称是否可用以 GitHub 创建页面为准）

## 仓库简介（Description）

基于 OP07 与 TL084 的心电信号模拟前端课程项目，包含仪用放大、50 Hz Fliege 陷波、四阶低通、电平抬升及右腿驱动，以及 Multisim 仿真、PCB 工程和实物调试记录。

## 项目主要内容

本项目围绕毫伏级心电信号的模拟调理展开，完成了方案设计、参数计算、Multisim 仿真、原理图与 PCB 设计以及实物焊接调试。主信号链由三运放仪用放大器、高通与可调增益级、50 Hz Fliege 陷波器、四阶 Sallen-Key 低通滤波器和电平抬升电路组成，另设右腿驱动支路，用于心电模拟器条件下的共模反馈实验。

项目重点记录增益分配、工频抑制、精密电阻组合、滤波参数选择和实物校准方法，同时保留了制板与调试过程中发现的问题及修正记录。仓库提供可打开的仿真工程、EDA 工程、设计笔记和实验报告，供模拟电路课程学习与实验复现参考。

本项目面向实验室信号源和心电模拟器，不用于人体连接或医疗诊断。

## 建议 Topics

```text
ecg analog-front-end analog-circuit instrumentation-amplifier
active-filter notch-filter multisim pcb op07 tl084
```

## 首页文件

- `README.md`：中文项目首页。
- `docs/assets/hero.svg`：首页封面。
- `docs/assets/signal-chain.svg`：信号链路图。
- `docs/assets/pcb-board.jpg`：报告中的 PCB 实物照片。

上传时保留目录结构，否则 README 中的图片会失效。原有工程、设计笔记和报告也应按 README 的相对路径放置。

## 发布前确认

1. 检查报告内的姓名、学号和照片，确认哪些信息适合公开。
2. 明确工程版本，说明实物修正是否已经回标；不要把旧版工程标记为最终复现版本。
3. 当前未添加许可证；如需授权他人复用，可自行选择适用许可证后新增 `LICENSE`，不要直接写成 MIT 或其他未确认的许可。
4. 本次只整理本地发布材料，没有创建远程仓库、上传文件或执行 Git 提交。
