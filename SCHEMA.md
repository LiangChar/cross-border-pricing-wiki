# Wiki Schema

## Domain
跨境电商定价与调价知识库 — 涵盖定价策略、成本核算、利润分析、库存周转、动态调价的公式和实践。

## 数据源背景
- **飞书电子表格**：店铺活动表（含采购价、销量、库存、库龄、动销天数等字段）
- **飞书多维表格**：库存统计表（含海外仓库存、锁定库存、超卖判定等字段）
- 不含第三方 ERP，所有定价/调价逻辑基于自有表格数据

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `pricing-formula.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- **Provenance markers:** On pages that synthesize 3+ sources, append `^[raw/articles/source-file.md]` at the end of paragraphs

## Frontmatter
```yaml
---
title: 页面标题
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
---
```

## Tag Taxonomy
- 定价: pricing, cost-plus, value-based, dynamic-pricing, psychological-pricing
- 成本: cost-structure, procurement, logistics, platform-fee, tariff, exchange-rate
- 利润: profit-margin, roi, break-even, net-profit
- 库存: inventory-turnover, safety-stock, replenishment, warehouse-age, overstock
- 调价: price-adjustment, price-optimization, clearance, promotion
- 数据: feishu-spreadsheet, feishu-bitable, formula, dashboard
- 策略: strategy, competitive-analysis, lifecycle-pricing
- 平台: amazon, shopee, lazada, shein

Rule: every tag on a page must appear in this taxonomy. Add new tags here first.

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions
- **Split a page** when it exceeds ~200 lines

## Update Policy
When new information conflicts with existing content:
1. Check dates — newer sources supersede older ones
2. If contradictory, note both positions with dates and sources
3. Flag for review
