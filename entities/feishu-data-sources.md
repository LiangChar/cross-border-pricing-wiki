---
title: 飞书数据源（定价相关）
created: 2026-05-25
updated: 2026-05-25
type: entity
tags: [feishu-spreadsheet, feishu-bitable, data]
sources: []
---

# 飞书数据源（定价相关）

## 电子表格：店铺活动表
- **token**: `HoTusM4xahtMaBtWDA8cVTSAn6u`
- **主 Sheet "总" ID**: `NKXU1U`
- **数据量**: ~5417 行，25 个 Sheet

### 定价相关列

| 列 | 字段名 | 定价用途 |
|----|--------|---------|
| A | 部门 | 按产品线分类定价 |
| C | 货号 | 产品唯一标识 |
| D | 自编SKU | 调价目标唯一标识 |
| E | 采购价 | 成本基数 |
| G | 月总销量 | 需求规模 |
| H | 近7日总销量 | 短期趋势 |
| I | 近7日平均总销量 | 日均基准 |
| J | 在售库存 | 供需关系 |
| K | 动销天数 | 周转速度 |
| L | 最长库龄(天) | 清仓信号 |
| R-BR | 店铺状态 | 登记/上架状态 |

## 多维表格：库存统计表
- **app_token**: `Cf5zbg4nlauRyNslxDXcvbJYnJf`
- **table_id**: `tblSXRukbkcdIrRu`
- **数据量**: ~2175 条

### 关键字段

| 字段 | 用途 |
|------|------|
| 海外仓库存总计 | 可售库存量 |
| 锁定库存 | 不可用库存 |
| 超卖判定 | 库存-锁定<0 |
| 库龄 | 仓储时长 |
| 近7销量总计 | 近期需求 |
| 自编SKU | 关联标识 |

## 参见
- [[data-driven-pricing]] — 如何用这些数据做自动化定价
- [[pricing-formula]] — 公式中哪些参数来自这些表
- [[inventory-management]] — 库存数据如何驱动调价
