---
width: "1920"
height: "1080"
---

## 问题

- 整形手术预测
- **Input**: 术前骨骼 + 术前外形 + 术后骨骼
- **Output**: 术后外形
- **Method**: 物理模拟

---

## 当前进展

- 注册 + **模拟** + 评估
- 完成中期论文 (50%)
- 部分完成汇报 PPT

---

### 上周问题

- $K x + b = 0$
- 当 Poisson's ratio $\nu > 0.3$ 时, 解会崩掉
- 不是求解器的问题
- $K, b$ 有问题?

--

### 可能的方法

- 以下方法在数学上是等价的:
- 基于 $f = K x$ 求解 $K x + b = 0$
  - 已经试过的一些方法 ...
  - local steepest gradient method: $x_j = - K_{jj}^{-1} (\sum_k K_{jk} x_k)$
- 求解动力学方程 $M \frac{\partial^{2}x}{\partial t^2} + D \frac{\partial x}{\partial t} + \frac{\partial W}{\partial x} = 0$
  - 微分方程不一定容易求解
  - Projective Dynamics: 原理上不如其他方法有说服力
- 最小化能量 $W$
  - 没看到有工作这么做
  - 能量的选择可以比较自由

---

## 优先级较靠后的想法

- \[1\]: 即使 self-intersection / non-manifold 也可以生成 tetrahedral mesh
  - 可以保留原有表面的顶点
  - 降低 registration 的要求, 可能增加 simulation 的难度
- 允许 TetGen 在表面插入点
  - 提高 tet mesh 的质量
  - 插入的顶点可以用插值确定术后位置

---

## TODO

- 完成中期汇报, 补充配图
- 尝试不同的模拟方法
