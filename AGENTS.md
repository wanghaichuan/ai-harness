# AGENTS.md — AI Agent 入口导航（模板）

> **角色：地图，不是百科全书。** 复制本模板后按项目实际路径改链接。

## 进入项目第一步

1. **架构速查**：`docs/architecture/index.md`
2. **隐性约定（必读）**：`docs/architecture/implicit-contracts.md`
3. **产品规则**：`docs/product/index.md`
4. **AI 协作流程**：`docs/guides/AI开发写作维护指南.md` — 标准定位、开发流程、修改、验证、工作流
5. **业务词定位**：`docs/guides/业务词到代码入口索引.md`

## 编码前置动作（强制）

1. `codegraph status` → 不新鲜则 `codegraph sync`
2. 检查并更新项目记忆（`MEMORY.md` 体系）

未完成不写代码。

## 变更流程（强制执行）

```
propose（提案）  →  apply（实施）  →  verify（对齐校验）  →  archive（归档）
```

**铁律：没有 change 工件，不允许修改代码。** 工件位于 `openspec/changes/<中文change名>/`：`提案.md` + `设计.md` + `任务.md`。

## 评审流程（apply 后、archive 前）

1. 评审摘要（prepare-review）
2. 分层架构检查
3. SQL 风险检查
4. 独立只读评审（reviewer agent）

## 硬护栏

- 不允许直接修改环境配置（yml/properties）
- **数据库脚本由人手动执行，禁止 AI 自行执行**（AI 只编写和检查脚本）
- 不允许执行 `git push`、`kubectl`、`rm -rf` 等危险命令
- 不允许跳过工件流程写代码
