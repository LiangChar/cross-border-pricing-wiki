# Wiki Log

> Chronological record of all wiki actions. Append-only.

## [2026-05-25] create | Wiki initialized
- Domain: 跨境电商定价与调价
- Data sources: 飞书电子表格 + 多维表格（店铺活动表、库存统计表）
- Structure: SCHEMA.md, index.md, log.md, raw/, entities/, concepts/, comparisons/, queries/

## [2026-05-25] ingest | 批量入库
- raw/articles/10100-pricing-formula-manual.md — 跨境电商必备公式手册（8模块+25公式）
- raw/articles/baoguane-pricing-strategy-guide.md — 跨境电商定价策略指南

## [2026-05-25] create | 批量创建知识页
- concepts/pricing-formula.md — 定价公式总览
- concepts/profit-calculation.md — 利润核算
- concepts/inventory-management.md — 库存管理公式
- concepts/pricing-strategies.md — 定价策略类型
- concepts/cost-structure.md — 成本结构
- concepts/data-driven-pricing.md — 数据驱动定价
- concepts/price-adjustment-strategy.md — 调价策略
- concepts/clearance-pricing.md — 清仓定价
- entities/feishu-data-sources.md — 飞书数据源
- entities/inventory-strategy-rules.md — 库存管理策略
- comparisons/platform-commission-comparison.md — 平台佣金对比
- comparisons/pricing-strategy-comparison.md — 定价策略对比

## [2026-05-25] update | 更新 index.md — 12个页面全部索引

## [2026-05-26] update | 数据验证+策略修正
- 验证结论：降价97.7%无效，仓租不参与定价
- 数据源更新：4仓库仓租 + 折后价(MXN) + 在途数据
- 判定标准修正：库龄≥30天 + 无在途 → 真滞销
- 折扣逻辑修正：库龄×销量驱动，仓租只用于退仓建议
- 平台规则接入：TK秒杀折后最低价约束，TK折扣≤均价85%
- 更新页面：clearance-pricing, price-adjustment-strategy, data-driven-pricing
