# 年度报税资料整理流程

*中文 · [English](../annual-workflow.md)*

## 1. 确定范围

- 明确财年起止日、纳税人和资产持有比例。
- 记录本年变化：新工作、新课程、新设备、再融资、搬家、出租状态变化、证券出售。
- 不因“没有出售股票”而忽略股息、基金分配、AMIT 或境外收入。

## 2. 资料归档

建议本地目录：

```text
tax-YYYY-YY/
  00-summary/
  01-bank/
  02-income/
  03-rental/
  04-work-expenses/
  05-education/
  06-investments/
  07-health-and-medicare/
  08-prior-year/
```

原始文件只读保存；分析结果另建 Markdown 或工作簿。文件名包含日期、机构、项目和金额，但避免把 TFN 写入文件名。

## 3. 银行流水标准化

统一字段：

| 字段 | 说明 |
| --- | --- |
| date | 实际交易日期 |
| account | 银行及账户别名，不记录完整账号 |
| owner | 账户持有人别名 |
| amount | 收入为正、支出为负 |
| description | 银行原始描述 |
| merchant | 规范化收款人 |
| category | 租金、利息、保险、学习、设备、订阅等 |
| tax_status | confirmed / conditional / excluded / missing-evidence |
| evidence | 对应凭证文件或邮件主题 |
| notes | 地址、用途、工作比例等判断依据 |

先按收款人聚合，再检查大额、重复金额、周期性付款和模糊描述。信用卡还款、账户互转和投资账户入金不是费用本身，应追溯原交易。

PDF 流水可能在同一文件中包含多个子账户。必须逐页识别账户标题和交易区间，不能只读取首页汇总或第一张交易表。所有账户完成标准化后，先做账户级期初余额、流入、流出和期末余额校验，再进入税务分类。

## 4. Gmail 检索顺序

按财年限制日期，依次搜索：

- 工资及 PAYG：payslip、income statement；
- 出租房：物业地址、中介名称、rental statement、levy、rates、water、insurance、repair；
- 工作费用：invoice、subscription、software、membership、registration、CPD；
- 学习：学校名称、student account、tax invoice、Commonwealth Assistance Notice；
- 设备：Apple、JB Hi-Fi、电脑和手机型号；
- 税务管理：tax agent、accountant、lodgement fee。

邮件主题或银行描述只能作为线索。最终确认至少需要日期、金额、供应商、用途和付款人能相互匹配。

## 5. 收入核对

- 银行工资入账用于发现雇主、漏月和第二份工作，但不能代替 ATO Income Statement。
- 对每个雇主分别核对工资入账月份、ATO gross income 和 PAYG withholding。
- 工资净入账与 gross income 的差异通常包含 PAYG、养老金外项目、包装或其他扣款；不要反推后直接申报。
- 相同姓名账户间、夫妻账户间和储蓄账户间的转账标为内部转账，不算家庭收入。
- 没有卖出证券不代表没有投资收入；仍要检查利息、股息、基金分配、AMIT 和境外收入。

## 6. 分类规则

- `confirmed`：付款与凭证、用途和财年均匹配。
- `conditional`：交易真实，但税务资格依赖工作关系、使用比例或课程性质。
- `excluded`：私人支出、资本投入、账户互转、已报销或重复费用。
- `missing-evidence`：金额或收款人看似相关，但缺发票、地址或项目说明。

## 7. 跨年检查

每年必须回看上一年工作簿和最终申报：

- 电脑、手机及其他设备的 adjustable value；
- borrowing expenses 的剩余年度；
- capital works 和 quantity surveyor schedule；
- 上一年实际支付的 tax-agent fee；
- 未抵扣税务亏损；
- 跨财年预付款；
- 已付款但上一年因日期或凭证不足而暂缓的项目。

不要把“去年购买”直接等同于“今年可扣”。应查看折旧表、发生/支付日期和既往申报记录。

## 8. 输出

至少交付三份结果：

1. 当前估算和假设；
2. 银行流水逐项判断；
3. 缺件和待确认问题。

所有数字都应能追溯到来源；保守确认额和高可信候选额应分开显示。
