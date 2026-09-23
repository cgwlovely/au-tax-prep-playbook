# 收入与家庭现金流对账

本流程同时支持报税资料核对和家庭资金去向分析，但两者必须使用不同口径。报税按税务性质分类，家庭现金流按真实流入、真实消费、资产转移和内部转账分类。

## 数据覆盖

建立账户清单，逐一记录账户持有人别名、机构、账户类型、覆盖日期、期初和期末余额。银行 PDF 内含多个子账户时，每个子账户单独登记。缺少一个账户或一个月份时，汇总结论标为不完整。

## 标准字段

```text
date | owner | source | account | description | merchant
amount | flow_type | category | subcategory | tax_status
evidence | counterparty | transfer_match | notes
```

`flow_type` 至少包含：

- `income`：工资、租金、利息等外部流入；
- `expense`：商品或服务的最终消费；
- `internal-transfer`：本人账户或家庭共同账户间转账；
- `investment-or-debt`：证券入金、贷款本金、储蓄资产转移；
- `refund-or-reversal`：商户退款或冲正；
- `unresolved`：尚不能确定性质的交易。

## 工资收入

1. 从银行流水识别所有周期性工资入账，并按雇主规范化名称。
2. 检查漏月、一次性奖金、离职付款和第二雇主。
3. 使用 ATO Income Statement 确认每个雇主的 gross income 和 PAYG withholding。
4. 银行收到的净工资只用于现金流和完整性检查，不直接作为申报收入。

## 防止重复计算

- 两个家庭账户之间同日、近似金额的出入账应配对为内部转账。
- 信用卡或分期账户还款不是第二次消费；若已有底层购买明细，排除还款。
- 券商入金和储蓄账户转入是资产转移，不归入生活消费。
- 商户退款应与原支出配对；无法配对时单列，不要直接抵销整个类别。
- 现金提取、模糊转账和支付平台交易在确认最终收款人前保持 `unresolved`。

## 家庭收支平衡

账户级先验证：

```text
opening balance + external inflows + internal inflows
- external outflows - internal outflows = closing balance
```

家庭级再抵销内部转账：

```text
external income - real expenses
- net investment/debt funding + refunds
= change in household cash, allowing for opening/closing timing
```

报告至少分开展示：工资及其他收入、住房、食品、交通、医疗保险、教育、订阅、设备、投资/债务、退款和待识别项目。不要用“其他”掩盖金额较大或周期性的商户。

## 商户识别和凭证匹配

先按原始描述建立商户别名字典，再结合发票日期、金额、邮箱收件人、订单号和用途确认。水电网、保险、市政费、物业费和订阅应检查周期完整性；发现缺月或金额异常时，回查邮件账单或对应账户。

## 输出质量门槛

- 所有账户和月份均有覆盖状态；
- 内部转账配对率和未配对金额可见；
- 未识别交易单独列示；
- 收入同时给出银行净收入口径和 ATO 税务口径；
- 每个汇总数字可下钻到原交易和凭证；
- 报税候选与普通家庭消费严格分开。
