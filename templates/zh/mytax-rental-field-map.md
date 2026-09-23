# myTax 出租房字段对照模板

*中文 · [English](../mytax-rental-field-map.md)*

复制到新财年后逐格填写。金额按**本人持有比例**填写；若页面要求先填全额再选比例，则填全额栏。

## 房产信息

| myTax 字段 | 内容 |
| --- | --- |
| Property address | |
| Date property first earned rental income | |
| Number of weeks property was rented | |
| Your ownership percentage | |
| Was the property available for rent all year? | |

## 收入

| myTax 字段 | 中文 | 本人份额 | 全额 | 来源 |
| --- | --- | ---: | ---: | --- |
| Gross rent | 租金总收入 | | | 中介年度 summary |
| Other rental related income | 其他出租相关收入 | | | 各类补偿、退款、保险赔付 —— 见下方说明 |

> **每一笔退款、赔付、保险理赔或补贴，在性质确定之前一律标为 `conditional`。** 有的属应税收入，有的冲减 cost base，有的触发折旧资产的 balancing adjustment。先定性质，再决定填哪一栏。

> 最明确的一种情形：租客就损坏向你付款、而你又扣除了该项维修支出的，收到的**全额**计入收入。资本性项目的保险理赔、折旧资产的补贴、以及用押金抵欠租，三者处理各不相同。

> 永远错误的做法是：支出照扣，收到的补偿不报。本行存在的意义就是防止这一点。

## 支出

| myTax 字段 | 中文 | 本人份额 | 全额 | 归集说明 |
| --- | --- | ---: | ---: | --- |
| Advertising for tenants | 招租广告 | | | |
| Body corporate fees and charges | 物业费 | | | 中介代付 + 业主直付合并 |
| Borrowing expenses | 借款费用摊销 | | | 按 5 年**或贷款期限，取较短者**摊销。合资格借款费用合计不超过 $100 的，当年全额扣除。提前全额还清贷款的，余额在还清当年一次扣除。 |
| Cleaning | 清洁 | | | |
| Council rates | 市政费 | | | 仅出租房部分 |
| Capital works deductions | 资本工程 Div 43 | | | 能取得实际建造成本的，用实际成本。**只有在无法取得时**，才需要合格人士出具的合理估算（TR 97/25）。先筛建成年份，见 [维修、改良与折旧资格](../../docs/zh/repairs-vs-capital.md)。 |
| Decline in value of depreciating assets | 设备折旧 Div 40 | | | 仅自购全新资产 |
| Gardening/lawn mowing | 园艺除草 | | | |
| Insurance | 保险 | | | **承保出租房**的险种 —— building、contents、public liability、loss of rent 均可。判断标准是保单保什么，不是产品名称是否叫 landlord insurance。自住房的保单不能填在这里；同一保险公司多张保单的分流见 [费用归属判定](../../docs/zh/expense-attribution.md)。 |
| Interest on loans | 贷款利息 | | | 只扣利息，不含本金 |
| Land tax | 土地税 | | | |
| Legal fees | 法律费用 | | | |
| Pest control | 虫害防治 | | | |
| Property agent fees/commission | 中介管理费与佣金 | | | 管理费 + 出租佣金 |
| Repairs and maintenance | 维修与保养 | | | 已剔除折旧与资本工程部分 |
| Stationery, telephone, postage | 文具电话邮费 | | | |
| Travel expenses | 差旅 | | | 住宅出租房自 2017-07-01 起不可扣 |
| Water charges | 水费 | | | 仅出租房部分 |
| Sundry rental expenses | 其他杂项 | | | 烟感检测、测量师费用等 |

## 核对

```text
收入合计 - 支出合计 = 出租房净额
各持有人份额之和 = 房产总额
```

myTax 算出的净额应与自建工作簿一致。不一致时逐项回查，不要调整任一侧凑平。

## 容易填错的地方

- 把自住房的市政费、水费填进出租房；
- 把中介净转账当作 Gross rent（应填中介 summary 的 Money In）；
- 中介已代付的费用，又按发票原件重复列支；
- 把整机更换的设备填进 Repairs and maintenance（应走 Div 40）；
- 把资本性改良填进 Repairs and maintenance（应走 Div 43）；
- 漏填 Other rental related income 中的退款与赔付。
