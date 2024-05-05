## 问题

- 整形手术预测
- **Input**: 术前骨骼 + 术前外形 + 术后骨骼
- **Output**: 术后外形
- **Method**: 物理模拟

---

## 上周进展

- DONE 实现对穿模 mesh 的 tetrahedralization
- TODO 在数据集上完成量化评估
- TODO 调研 CG physics 方向

---

## 穿模 Mesh 的 Tetrahedralization

- 动机: 降低对 registration 的要求
- 方法:
  - 先 "修好" 穿模, 再插值
- 可以处理:
  - 上 / 下颌骨 / 外表面自相交, 上下颌骨互穿
- 不能处理:
  - 骨骼和外表面的穿模 (一般不会出现)

```shell
paraview tetra.vtu
meshlab {pre,post}-*.ply
```

---

## TODO

- 准备在数据集上量化评估
  - 目前有 23 组 CT
- 可视化 \& 撰写论文 (DDL 05.26)
- 调研图形学 physics 方向
