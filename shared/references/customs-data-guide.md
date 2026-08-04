# 海关数据应用指南

> 海关数据是外贸客户开发中**唯一无法造假的真实交易记录**。用好它，你能知道谁在买、买了多少、从哪买、多少钱。

---

## 一、海关数据能回答的10个关键问题

```yaml
customs_data_can_answer:
  q1: "这个客户真的在进口烤箱/烟机吗？→ 查HS Code进口记录"
  q2: "这个客户每年进口多少？→ 数量+金额+频率"
  q3: "这个客户从哪些国家采购？→ 出口国分布"
  q4: "这个客户的现有供应商是谁？→ 出口商名称"
  q5: "竞争对手把货卖给了谁？→ 反查竞品出口记录"
  q6: "这个国家的进口量在增长还是下滑？→ 趋势分析"
  q7: "这个客户的采购季节是什么时候？→ 月度进口分布"
  q8: "客户的采购单价大约是多少？→ 金额÷数量=参考单价"
  q9: "这个客户是新买家还是老买家？→ 进口历史长度"
  q10: "这个市场有哪些新买家？→ 近期首次进口的企业"
```

---

## 二、立式烤箱与烟机的HS Code

### 立式烤箱

| HS Code | 描述 | 覆盖产品 |
|---------|------|---------|
| **7321.11** | Gas cooking appliances (燃气烹饪器具) | 燃气立式烤箱、燃气灶烤箱一体机 |
| **7321.90** | Parts of gas cooking appliances | 燃气灶烤箱配件 |
| **8516.60** | Electric ovens/cookers (电烤箱/电灶) | 电立式烤箱、电灶烤箱一体机 |
| **8516.90** | Parts of electric ovens | 电烤箱配件 |

### 烟机

| HS Code | 描述 | 覆盖产品 |
|---------|------|---------|
| **8414.60** | Ventilating/recycling hoods (通风/循环烟机) | 所有类型的烟机 |
| **8414.59** | Other fans (其他风机) | 部分烟机可能归类于此 |

### 关联HS Code（套装采购信号）

| HS Code | 描述 | 意义 |
|---------|------|------|
| **7321.11 + 8414.60** | 同一进口商同时进口燃气灶和烟机 | 🟢 高价值客户 — 很可能采购烟灶套装 |

---

## 三、主要海关数据平台

```yaml
platforms:
  global:
    - name: "Panjiva (S&P Global)"
      coverage: "全球主要贸易国"
      strength: "数据完整、搜索灵活"
      cost: "$$$ 企业订阅"
      
    - name: "ImportGenius"
      coverage: "美国、南美、亚洲部分"
      strength: "美国数据最全、可追踪提单"
      cost: "$$ 月度订阅"
      
    - name: "TradeData.net"
      coverage: "全球200+国家"
      strength: "覆盖面广"
      cost: "$$ 按查询收费"
      
  china_specific:
    - name: "中国海关数据 / 海关总署"
      coverage: "中国进出口"
      strength: "最权威的中国出口数据"
      note: "部分省份/产品有详细公开数据"
      
    - name: "特易资讯 (Topease)"
      coverage: "中国+全球"
      strength: "中文界面、适合中国外贸企业"
      
    - name: "腾道 (Tendata)"
      coverage: "全球"
      strength: "性价比高、中小外贸企业常用"
      
  free_or_low_cost:
    - name: "UN Comtrade"
      coverage: "全球200+国家"
      strength: "免费、联合国官方"
      limitation: "数据滞后6-12个月、粒度粗"
      
    - name: "各国海关官网"
      coverage: "单个国家"
      strength: "免费、最权威"
      note: "美国USITC、欧盟Eurostat、日本Trade Statistics等"
      
    - name: "Trademap.org (ITC)"
      coverage: "全球"
      strength: "免费版可查基本趋势"
      limitation: "详细交易数据需付费"
```

---

## 四、客户发现：从海关数据找新客户

### 方法1：按HS Code搜索进口商

```
搜索策略：
1. 在海关数据平台输入 HS 7321.11（燃气烤箱）
2. 筛选目标国家
3. 按进口量降序排列
4. 导出前50-100家进口商
5. 排除已知品牌工厂（如Whirlpool自有工厂）→ 保留贸易商/品牌商/批发商
```

### 方法2：竞品反查——找到竞争对手的客户

```
这是海关数据最高价值的用法。

步骤：
1. 搜索已知竞争对手的出口记录（搜索竞品公司名）
2. 查看竞品的海外收货方（Consignee / Importer of Record）
3. 这些收货方 = 已验证有采购需求的客户
4. 分析竞品给他们的价格（数量÷金额）→ 我方报价参考
5. 用"产品线补充"或"替代供应商"角度切入

⚠️ 注意：
- 不要在首次联系时暴露你知道他们的供应商是谁
- 不要直接说"I know you buy from XXX"
- 用"我们注意到贵司在XX市场有厨房电器需求"这种表述
```

### 方法3：发现新买家

```
搜索条件：
- 时间范围：近6个月
- 进口频率：首次出现（之前12个月无记录）
- HS Code：7321.11 / 8414.60 等

新买家的价值：
- 没有固定供应商 → 切入难度低
- 正在建立供应链 → 决策速度快
- 价格敏感度较低 → 利润空间好
```

### 方法4：趋势发现——找到增长中的市场

```
分析维度：
- 某国家过去3年的烤箱/烟机进口量变化
- 进口来源国占比变化（中国份额在增加还是减少？）
- 单价变化趋势（高端化还是低价化？）

实操：
1. 在Trademap/UN Comtrade查目标国家 HS 7321.11 进口数据
2. 看3年趋势：进口量↑且中国占比↑ → 优先开发
3. 如果进口量↓或单价↓ → 谨慎开发
```

---

## 五、客户验证：用海关数据核实客户

### 验证清单

```yaml
customer_verification_via_customs:
  verify_importer:
    question: "这个客户真的有进口记录吗？"
    action: "搜索客户公司名或收货方名称"
    signals:
      green: "过去12个月有持续进口记录"
      yellow: "有进口记录但频率低（一年1-2次）"
      red: "海关数据完全找不到 → 可能不是直接进口商"
      
  verify_scale:
    question: "客户的采购规模多大？"
    action: "统计年度总进口量和柜数"
    signals:
      large: "年进口>100柜 → 大型进口商"
      medium: "年进口20-100柜 → 中型"
      small: "年进口<20柜 → 小型/新买家"
      
  verify_sourcing:
    question: "客户从哪些国家采购？"
    action: "查看进口来源国分布"
    signals:
      china_dominant: "70%+从中国采购 → 对中国供应链依赖高"
      diversified: "从多国采购 → 需要差异化切入"
      no_china: "从不从中国采购 → 可能存在偏见或认证壁垒"
      
  verify_seasonality:
    question: "客户什么时候采购？"
    action: "查看过去2年月度进口分布"
    value: "在客户采购季前2-3个月触达 → 回复率最高"
    
  verify_price:
    question: "客户的采购价位？"
    action: "CIF金额÷数量 = 参考单价"
    note: "注意这是CIF价（含运费保险），比FOB高约10-15%"
```

---

## 六、竞品分析：用海关数据了解竞争格局

### 竞品画像

```yaml
competitor_analysis:
  who_are_they:
    - "搜索目标市场中和你出口同类产品的中国公司"
    - "按出口量排序，找到Top 10中国出口商"
    
  who_are_their_customers:
    - "反查每个竞品的收货方"
    - "分析客户类型分布（进口商vs品牌商vs批发商）"
    
  what_is_their_pricing:
    - "竞品平均FOB单价 = 竞品出口金额 ÷ 数量"
    - "对比你的成本 → 判断价格竞争力"
    
  what_is_their_market_share:
    - "竞品在该国的出口量 ÷ 该国总进口量"
    - "找到份额在下降的竞品 → 他们的客户最容易被撬动"
```

### 竞品客户撬动策略

```yaml
competitor_customer_poaching:
  best_targets:
    - "竞品市场份额在下降 → 客户可能在寻找替代"
    - "客户从竞品采购但量在减少 → 不满意信号"
    - "客户同时从多个供应商采购 → 用差异化产品切入"
    
  worst_targets:
    - "客户与竞品有合资/关联关系"
    - "客户是竞品的独家代理"
    - "客户与竞品合作超过10年且量稳定上升"
    
  approach:
    angle_1: "补充产品线（客户从竞品买A类产品，你提供B类）"
    angle_2: "质量升级方案（不贬低竞品，只说'更好的选择'）"
    angle_3: "供应链灵活性（更小的MOQ、更快的交期、更灵活的付款）"
```

---

## 七、市场分析

### 目标市场选择

```yaml
market_selection:
  step_1_size: "该国年度烤箱/烟机进口总额 → 市场够不够大？"
  step_2_trend: "过去3年进口量变化 → 在增长还是萎缩？"
  step_3_china_share: "中国在该国进口中的占比 → 中国产品的接受度"
  step_4_price: "进口平均单价 → 你的产品定价是否匹配？"
  step_5_concentration: "进口商集中度 → 几个大买家还是很多小买家？"
  
  scoring:
    growing_market_china_rising: "🟢 优先开发"
    stable_market_china_stable: "🟡 正常开发"
    declining_market_china_falling: "🔴 谨慎/放弃"
```

### 立式烤箱全球进口趋势速查

| 区域 | 市场规模 | 增长趋势 | 中国份额 | 开发建议 |
|------|:------:|:------:|:------:|---------|
| 中东(沙特/阿联酋/伊拉克) | 大 | ↑增长 | 高 | 🟢 优先 |
| 非洲(尼日利亚/肯尼亚/加纳) | 中 | ↑快速增长 | 高 | 🟢 优先 |
| 东南亚(印尼/菲律宾/越南) | 中 | ↑增长 | 中高 | 🟢 优先 |
| 南美(巴西/智利/秘鲁) | 中 | →平稳 | 中 | 🟡 正常 |
| 欧洲(英/法/德) | 大 | →平稳 | 低 | 🟡 需认证 |
| 澳洲 | 小 | →平稳 | 中 | 🟡 需AGA认证 |
| 北美(美/加) | 大 | →平稳 | 低 | 🔴 需ETL/UL |

### 烟机全球进口趋势速查

| 区域 | 市场规模 | 增长趋势 | 中国份额 | 开发建议 |
|------|:------:|:------:|:------:|---------|
| 欧洲(德/法/意/英) | 最大 | →平稳 | 中 | 🟡 需品牌/设计 |
| 中东 | 大 | ↑增长 | 高 | 🟢 优先 |
| 东南亚 | 中 | ↑快速增长 | 高 | 🟢 优先 |
| 南美 | 中 | ↑增长 | 高 | 🟢 优先 |
| 北美 | 大 | →平稳 | 低 | 🔴 需ETL |
| 非洲 | 小→中 | ↑快速增长 | 高 | 🟢 培育市场 |

---

## 八、海关数据在评分中的应用

### 采购信号加分规则

```yaml
customs_data_scoring:
  has_import_record_12m:
    score: "采购可能性 +5"
    condition: "过去12个月有匹配HS Code的进口记录"
    
  consistent_importer:
    score: "采购可能性 +3"
    condition: "连续2年以上有进口记录，频率稳定"
    
  growing_importer:
    score: "采购可能性 +4"
    condition: "近1年进口量同比增长>20%"
    
  china_sourced:
    score: "采购可能性 +2"
    condition: "进口来源中有中国（占比>30%）"
    
  first_time_buyer:
    score: "采购可能性 +3, OEM潜力 +2"
    condition: "过去6个月内首次出现进口记录"
    
  competitor_customer:
    score: "采购可能性 +4"
    condition: "是已知竞品的客户 → 有验证过的采购需求"
```

---

## 九、实操工作流

### 每日海关数据工作流（15-30分钟）

```yaml
daily_customs_routine:
  step_1_discover:
    action: "搜索目标HS Code + 目标国家，查看近1周新记录"
    time: "5分钟"
    output: "新进口商、新买家、新增的竞品客户"
    
  step_2_verify:
    action: "将昨日采集的客户名单跑一遍海关数据验证"
    time: "5分钟"
    output: "标记有进口记录的客户 → 提升评分"
    
  step_3_competitor:
    action: "反查1-2个竞品的近期出口记录"
    time: "5分钟"
    output: "竞品新客户、竞品客户流失信号"
    
  step_4_trend:
    action: "查看目标市场的月度进口数据变化"
    time: "5分钟"
    output: "趋势变化、季节性判断"
```

---

## 十、注意事项

```yaml
caveats:
  data_lag:
    note: "海关数据通常有1-3个月延迟。刚发生的交易可能还查不到。"
    
  data_granularity:
    note: "不同国家数据粒度不同。美国的数据最详细（提单级别），有些国家只有HS 6位码级别。"
    
  cif_vs_fob:
    note: "进口数据通常是CIF价格（含运费保险），做价格对比时要减去10-15%。"
    
  company_name_variations:
    note: "同一家公司可能有多个名称变体（子公司、贸易主体、缩写），搜索时要注意。"
    
  not_all_countries_available:
    note: "并非所有国家都公开海关数据。中东、非洲部分国家数据不全。"
    
  privacy_shields:
    note: "部分国家允许进口商隐藏公司名（如巴西、越南部分记录），这些记录只能看到国家看不到公司。"
    
  do_not_misuse:
    note: "海关数据用于商业开发和市场研究。不得用于非法用途或违反数据使用条款。"
```
