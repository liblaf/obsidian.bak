## 问题

- 整形手术预测
- **Input**: 术前骨骼 + 术前外形 + 术后骨骼
- **Output**: 术后外形
- **Method**: 物理模拟

---

## 上周进展

- DONE 跑通一组 pipeline
  - 无需 landmarks
  - Poisson's ratio $\nu = 0.25$ (ref. $\nu = 0.46$)
  - 约 20 min (其中 registration > 15 min)
  - TetGen 不鲁棒 (暂不清楚原因, 与编译选项和浮点计算有关)
- TODO 调研 CG physics 方向

---

## Example Results

```shell
paraview target/120056/{tetra,predict,ground-truth}.vtu target/120056/{pre,post}/99-{mandible,maxilla}.vtu # simulation
paraview target/120056/post/02-{face,skull}.ply target/120056/post/99-{face,mandible,maxilla}.vtu # registration
```

---

## TODO

- 跑完所有 (能跑通) 数据, 共 23 组
- 可视化 \& 撰写论文 (DDL 05.26)
- 调研图形学 physics 方向
