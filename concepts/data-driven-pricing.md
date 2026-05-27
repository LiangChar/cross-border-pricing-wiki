---
title: 数据驱动定价与自动化（已验证版）
created: 2026-05-25
updated: 2026-05-26
type: concept
tags: [data, feishu-spreadsheet, feishu-bitable, formula, verified]
sources: [raw/articles/10100-pricing-formula-manual.md]
---

# 数据驱动定价与自动化（已验证版）

## 数据源全景

### 主数据：飞书电子表格（店铺活动表）
- token: `HoTusM4xahtMaBtWDA8cVTSAn6u`
- 主Sheet "总": `NKXU1U`
- 定价用字段: A=部门 C=货号 D=自编SKU E=采购价 F=头程 G=月总销量 H=近7日总销量 I=近7日平均总销量 J=在售库存 K=动销天数 L=最长库龄

### 销量数据：近7日销量统计表（Bitable）
- app_token: `Cf5zbg4nlauRyNslxDXcvbJYnJf`
- table_id: `tblaOxggbSpvSino`
- 约3739条记录
- 关键字段：
  - `折后价(MXN)` — 实际成交价（用于均价计算）
  - `近7天折后价` — 价格历史数组 [最新...最旧]
  - `近7总销量引用` — 全店铺近7日总销量
  - `本人店铺总销量` — 本店销量

### 仓租数据：4仓库明细
- MX394: tblCttyuGDheupoK (2774条)
- XH151: tblpbuvtmKIgZWoU (2689条)
- XH152: tblaftTasWDbJlIU (55条)
- MX491: tblx9UPar6KSD0Gm (985条)
- 共6503条，68个SKU多仓存储
- 关键字段: `仓租金额(MXN)`, `仓租单价(MXN)`, `库龄(天)`

### 在途数据：库存统计表
- table_id: tblSXRukbkcdIrRu
- 约2424 SKU，933个有在途
- 关键字段: `2025海外在途货值`, `2026海外在途货值`

## 滞销品判定标准（已验证）

必须同时满足：
1. 库龄 ≥ 30天（排除新品）
2. 动销天数 > 30天（排除正常品）
3. 无在途库存（排除已补货品）

## 折后价计算方法

**来源**：近7日销量统计表 `折后价(MXN)` 字段
**方法**：同一SKU在不同店铺的折后价去重后取最低和均价
**注意**：不用 `单品售价(MXN)` — 该字段含旧值污染

## 参见
- [[pricing-formula]] — 定价公式
- [[clearance-pricing]] — 清仓定价
- [[price-adjustment-strategy]] — 调价策略
