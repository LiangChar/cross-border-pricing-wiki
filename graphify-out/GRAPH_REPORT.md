# Graph Report - .  (2026-05-26)

## Corpus Check
- Corpus is ~2,765 words - fits in a single context window. You may not need a graph.

## Summary
- 31 nodes · 64 edges · 6 communities (5 shown, 1 thin omitted)
- Extraction: 92% EXTRACTED · 8% INFERRED · 0% AMBIGUOUS · INFERRED: 5 edges (avg confidence: 0.81)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_定价公式与成本核算|定价公式与成本核算]]
- [[_COMMUNITY_决策指标与清仓信号|决策指标与清仓信号]]
- [[_COMMUNITY_库存管理与清仓策略|库存管理与清仓策略]]
- [[_COMMUNITY_飞书数据源与自动化|飞书数据源与自动化]]
- [[_COMMUNITY_定价策略类型与对比|定价策略类型与对比]]
- [[_COMMUNITY_配置项|配置项]]

## God Nodes (most connected - your core abstractions)
1. `跨境电商定价公式` - 11 edges
2. `数据驱动定价与自动化` - 11 edges
3. `跨境电商库存管理公式` - 10 edges
4. `跨境电商调价策略` - 9 edges
5. `跨境电商成本结构` - 8 edges
6. `跨境电商必备公式手册（10100文章）` - 8 edges
7. `跨境电商利润核算` - 7 edges
8. `跨境电商定价策略类型` - 7 edges
9. `清仓定价策略` - 7 edges
10. `飞书数据源（定价相关）` - 6 edges

## Surprising Connections (you probably didn't know these)
- `超卖预警（库存−锁定<0）` --conceptually_related_to--> `调价决策矩阵`  [INFERRED]
  entities/feishu-data-sources.md → concepts/price-adjustment-strategy.md
- `飞书数据源（定价相关）` --references--> `跨境电商定价公式`  [EXTRACTED]
  entities/feishu-data-sources.md → concepts/pricing-formula.md
- `跨境电商定价公式` --shares_data_with--> `飞书店铺活动表`  [EXTRACTED]
  concepts/pricing-formula.md → entities/feishu-data-sources.md
- `跨境电商成本结构` --cites--> `跨境电商定价策略指南（包关网文章）`  [EXTRACTED]
  concepts/cost-structure.md → raw/articles/baoguane-pricing-strategy-guide.md
- `清仓定价策略` --cites--> `跨境电商必备公式手册（10100文章）`  [EXTRACTED]
  concepts/clearance-pricing.md → raw/articles/10100-pricing-formula-manual.md

## Communities (6 total, 1 thin omitted)

### Community 0 - "定价公式与成本核算"
Cohesion: 0.43
Nodes (8): ACOS（广告销售成本）, 成本加成定价, 跨境电商成本结构, 跨境电商平台佣金对比, 考虑平台佣金的精确定价, 跨境电商定价公式, 跨境电商利润核算, 跨境电商必备公式手册（10100文章）

### Community 1 - "决策指标与清仓信号"
Cohesion: 0.40
Nodes (5): 调价决策矩阵, 清仓决策流程（库龄>90天/196天）, 隐性成本（退款/汇率/仓租）, 库存周转率, ROI（投资回报率）

### Community 2 - "库存管理与清仓策略"
Cohesion: 0.70
Nodes (5): 清仓定价策略, 跨境电商库存管理公式, 库存管理策略（业务规则）, 跨境电商调价策略, 补货点计算

### Community 3 - "飞书数据源与自动化"
Cohesion: 0.70
Nodes (5): 数据驱动定价与自动化, 飞书库存统计表, 飞书数据源（定价相关）, 飞书店铺活动表, 超卖预警（库存−锁定<0）

### Community 4 - "定价策略类型与对比"
Cohesion: 0.50
Nodes (5): 动态定价, 渗透定价（新品低价入市）, 跨境电商定价策略类型, 定价策略适用场景对比, 跨境电商定价策略指南（包关网文章）

## Knowledge Gaps
- **2 isolated node(s):** `newLinkFormat`, `useMarkdownLinks`
  These have ≤1 connection - possible missing edges or undocumented components.
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `跨境电商定价公式` connect `定价公式与成本核算` to `库存管理与清仓策略`, `飞书数据源与自动化`, `定价策略类型与对比`?**
  _High betweenness centrality (0.206) - this node is a cross-community bridge._
- **Why does `跨境电商定价策略类型` connect `定价策略类型与对比` to `定价公式与成本核算`, `库存管理与清仓策略`?**
  _High betweenness centrality (0.141) - this node is a cross-community bridge._
- **Why does `数据驱动定价与自动化` connect `飞书数据源与自动化` to `定价公式与成本核算`, `库存管理与清仓策略`, `定价策略类型与对比`?**
  _High betweenness centrality (0.140) - this node is a cross-community bridge._
- **What connects `newLinkFormat`, `useMarkdownLinks`, `成本加成定价` to the rest of the system?**
  _8 weakly-connected nodes found - possible documentation gaps or missing edges._