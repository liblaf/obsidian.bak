## 问题

- 整形手术预测
- **Input**: 术前骨骼 + 术前外形 + 术后骨骼
- **Output**: 术后外形
- **Method**: 物理模拟

---

## 上周进展

- DONE 跑通一组 pipeline
  - 可以不用 landmarks
  - Poisson's ratio $\nu = 0.25$ (ref. $\nu = 0.46$)
  - 约 20 min (其中 registration > 15 min)
- TODO 调研 CG physics 方向

---

## TetGen 不鲁棒

- 暂不清楚具体原因, 有些错误肯能与编译选项和浮点计算相关
- 此前使用不考虑法向的 registration 能跑通 12 / 23 组

---

## Example Results

```shell
paraview target/120056/{tetra,predict,ground-truth}.vtu target/120056/{pre,post}/99-{mandible,maxilla}.vtu # simulation
paraview target/120056/post/02-{face,skull}.ply target/120056/post/99-{face,mandible,maxilla}.vtu # registration
```

---

## TODO

- 跑完所有 (能跑通的) 数据
- 可视化 \& 撰写论文 (DDL 05.26)
- 调研图形学 physics 方向
