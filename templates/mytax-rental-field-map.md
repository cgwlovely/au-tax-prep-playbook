# myTax 出租房字段对照模板

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
| Other rental related income | 其他出租相关收入 | | | 租客赔付、各类退款 |

> 退款与赔付必须两侧都申报 —— 收入侧记入本行，支出侧照常列支。只报一边是常见错误。

## 支出

| myTax 字段 | 中文 | 本人份额 | 全额 | 归集说明 |
| --- | --- | ---: | ---: | --- |
| Advertising for tenants | 招租广告 | | | |
| Body corporate fees and charges | 物业费 | | | 中介代付 + 业主直付合并 |
| Borrowing expenses | 借款费用摊销 | | | 贷款开办费五年摊销 |
| Cleaning | 清洁 | | | |
| Council rates | 市政费 | | | 仅出租房部分 |
| Capital works deductions | 资本工程 Div 43 | | | 需合格人士出具的估算 |
| Decline in value of depreciating assets | 设备折旧 Div 40 | | | 仅自购全新资产 |
| Gardening/lawn mowing | 园艺除草 | | | |
| Insurance | 保险 | | | 仅房东险 |
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
