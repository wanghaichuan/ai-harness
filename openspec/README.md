# openspec/ — 变更生命周期（规范）

## 目录结构

```
openspec/
└── changes/                  # 变更目录（保留，供后续变更使用）
    ├── README.md             # 本目录用处与规范说明
    ├── <中文change名>/       # 活跃变更，如：用户导出功能、订单结算改造
    │   ├── 提案.md           # 为什么改、范围边界
    │   ├── 设计.md           # 怎么改：方案、字段映射、接口
    │   ├── 任务.md           # 拆解清单（可勾选）
    │   └── （评审产物）       # review-summary / architecture-review / sql-review / review-report
    └── archive/              # 已完成变更归档
```

> 不设 `specs/`：系统工作原理归 `docs/architecture/` 与 `docs/product/`，避免职责重叠。

## 命名规范（重要）

- **change 目录用中文描述命名**（方便查找）：如 `用户导出功能`、`订单结算改造`
- **工件文件固定三个**：`提案.md`、`设计.md`、`任务.md`
- 评审产物追加在同目录，不与三大工件混名

## 四步流程

```
propose  →  apply  →  verify  →  archive
```

1. **propose**：建目录，产出三大工件
2. **apply**：严格按 `任务.md` 实施，不扩展需求
3. **verify**：与提案/设计对齐（不是代码风格审查）
4. **archive**：评审全过后移入 `archive/`
