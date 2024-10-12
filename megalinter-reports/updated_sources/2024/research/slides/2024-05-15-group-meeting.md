## 问题

- 整形手术预测
- **Input**: 术前骨骼 + 术前外形 + 术后骨骼
- **Output**: 术后外形
- **Method**: 物理模拟

---

## 上周进展

- DONE 跑了 10 组数据
- DOING 撰写论文 (70%)
- TODO 调研 CG physics 方向

---

## Accuracy

|       | Mean | STD  | 95%  | Max  |
|-------|------|------|------|------|
| Best  | 0.61 | 0.48 | 1.59 | 2.68 |
| Worst | 0.91 | 0.89 | 2.86 | 6.48 |

---

## Efficiency

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
