---
title: 清仓定价策略
created: 2026-05-25
updated: 2026-05-25
type: concept
tags: [clearance, price-adjustment, inventory-turnover, warehouse-age]
sources: [raw/articles/10100-pricing-formula-manual.md]
---

# 清仓定价策略

## 为什么清仓很重要

> 超过 28 周周转的产品，长期仓储费会持续侵蚀利润，越早清仓损失越小。

^[raw/articles/10100-pricing-formula-manual.md]

## 清仓决策流程

```
库龄 > 90天 + 无在途？
    ├── 是 → 加速清仓（降价 15-25%）
    │        └── 7天后仍无效果？
    │            └── 继续降价至成本价附近
    └── 否 → 跟踪观察
             └── 库龄 > 196天？
                  └── 是 → 必须清仓（降价 30-50%）
```

## 清仓定价方法

### 1. 阶梯降价法
每周降价 5%，观察销量反应。
- 优点：找到最优出清价格
- 缺点：周期长

### 2. 成本价出清
按采购价+运费出售，不赚利润只止损。
- 优点：快速出清
- 缺点：侵蚀品牌价格体系

### 3. 捆绑促销
滞销品 + 热销品组合出售。
- 优点：不影响单品价格认知
- 缺点：需要选品配合

## 与库存管理策略的对应

从 [[库存管理策略]]：
- 库龄 > 90 天且无在途 → 加速清仓（仓租收费高）
- 责任人：刘非凡、农敏、蔡慧丽、郑琅、杨欢

## 参见
- [[price-adjustment-strategy]] — 调价决策矩阵
- [[inventory-management]] — 库存管理公式
- [[data-driven-pricing]] — 自动化清仓信号
