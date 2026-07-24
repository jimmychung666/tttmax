# Appliance Export Deal OS

> 立式烤箱与烟机外贸客户开发成交 Skill 体系

**一句话定位**：面向立式烤箱和吸油烟机出口企业，将产品资料、目标市场和客户信息转化为精准客户画像、客户名单筛选、个性化触达、询盘分析、规格确认、OEM报价、持续跟进和订单成交方案。

**核心差异化**：这不是一个"写开发信的工具"，这是一个**教你如何做外贸生意的系统**。用了这个Skill，一个入行半年的新人，能做到5年经验外贸经理的水平。

---

## 📦 版本矩阵

| 版本 | 名称 | 定位 | 价格 | 目录 |
|------|------|------|------|------|
| 🆓 **免费版** | 家电客户资格评分器 | 获客引流+建立信任 | 免费 | [`free/`](free/) |
| 💰 **基础版** | 精准客户开发 Skill | 主力盈利产品 | ¥1,999/年 | [`basic/`](basic/) |
| 💎 **专业版** | Export Deal OS | 高客单价利润款 | ¥5,999/年 | [`professional/`](professional/) |
| 🏢 **企业版** | Export Deal OS Enterprise | 锚定价格天花板 | ¥29,800+/年 | [`enterprise/`](enterprise/) |

### 版本功能对比

| 核心能力 | 免费版 | 基础版 | 专业版 | 企业版 |
|---------|:----:|:----:|:----:|:----:|
| 产品档案建立 | 1个 | ✅ | ✅ | ✅ |
| 客户评分（单次） | 1次/天 | ✅ | ✅ | ✅ |
| 客户评分（批量） | ❌ | 20-50家 | ✅ | ✅ |
| 客户画像生成 | ❌ | 10种 | ✅ | ✅ |
| 搜索关键词生成 | ❌ | ✅ | ✅ | ✅ |
| 个性化开发邮件 | ❌ | ✅ | ✅ | ✅ |
| WhatsApp/LinkedIn | ❌ | ✅ | ✅ | ✅ |
| 询盘分析引擎 | ❌ | ❌ | ✅ | ✅ |
| 规格澄清向导 | ❌ | ❌ | ✅ | ✅ |
| OEM三档报价 | ❌ | ❌ | ✅ | ✅ |
| 智能跟进决策树 | ❌ | ❌ | ✅ | ✅ |
| 谈判助手 | ❌ | ❌ | ✅ | ✅ |
| 订单风险检查 | ❌ | ❌ | ✅ | ✅ |
| 自定义报价规则 | ❌ | ❌ | ❌ | ✅ |
| CRM对接 | ❌ | ❌ | ❌ | ✅ |
| 团队协作 | ❌ | ❌ | ❌ | ✅ |
| 私有部署 | ❌ | ❌ | ❌ | ✅ |

---

## 🗂️ 目录结构

```
CC/
├── README.md                          # 本文件
│
├── free/                              # 免费版
│   └── appliance-lead-scorer/
│       └── SKILL.md                   # 家电客户资格评分器
│
├── basic/                             # 基础版 ¥1,999/年
│   └── appliance-precision-outreach/
│       └── SKILL.md                   # 精准客户开发 Skill
│
├── professional/                      # 专业版 ¥5,999/年
│   └── appliance-export-deal-os/
│       └── SKILL.md                   # Export Deal OS (全流程)
│
├── enterprise/                        # 企业版 ¥29,800+/年
│   └── appliance-export-deal-os-enterprise/
│       └── SKILL.md                   # Enterprise
│
└── shared/                            # 共享资源
    ├── industry-packs/                # 行业知识包
    │   ├── freestanding-oven/         # 立式烤箱 (6个文件)
    │   │   ├── specifications.md      #   产品规格知识
    │   │   ├── buyer-types.md         #   客户类型画像
    │   │   ├── search-keywords.md     #   搜索关键词库
    │   │   ├── quotation-checklist.md #   报价检查清单
    │   │   ├── risk-checklist.md      #   风险检查清单
    │   │   └── pricing-rules.md       #   定价规则
    │   └── range-hood/                # 烟机 (6个文件)
    │       ├── specifications.md
    │       ├── buyer-types.md
    │       ├── search-keywords.md
    │       ├── quotation-checklist.md
    │       ├── risk-checklist.md
    │       └── pricing-rules.md
    │
    ├── references/                    # 规则参考 (9个文件)
    │   ├── security-classification.md # 安全与信息分级
    │   ├── sales-methodology.md       # 销售方法论
    │   ├── outreach-rules.md          # 个性化触达规则
    │   ├── qualification-rules.md     # 客户评分详细规则
    │   ├── quotation-rules.md         # 报价规则
    │   ├── risk-rules.md              # 风险检查规则
    │   ├── negotiation-rules.md       # 谈判与异议处理
    │   ├── follow-up-engine.md        # 智能跟进引擎
    │   └── pricing-engine.md          # 定价规则引擎
    │
    ├── templates/                     # 输入输出模板 (7个)
    │   ├── company-profile.json       # 企业档案模板
    │   ├── product-profile-oven.json  # 烤箱产品档案
    │   ├── product-profile-hood.json  # 烟机产品档案
    │   ├── lead-profile.json          # 客户档案模板
    │   ├── quotation-template.md      # 报价输出模板
    │   ├── follow-up-template.md      # 跟进输出模板
    │   └── risk-check-template.md     # 风险检查模板
    │
    └── config/                        # 配置文件 (2个)
        ├── scoring-rules.yaml         # 评分规则配置
        └── security-levels.yaml       # 安全分级配置
```

---

## 🚀 快速开始

### 免费版用户

1. 安装 `free/appliance-lead-scorer/SKILL.md`
2. 准备好你要评估的客户公司名+网站
3. 告诉Skill："帮我评估这个客户"并提供信息
4. 获得评分报告 + 开发建议

### 基础版用户

1. 安装 `basic/appliance-precision-outreach/SKILL.md`
2. 先建立产品档案（运行模块1）
3. 确定目标市场 → 生成客户画像（模块2）
4. 生成搜索方案 → 采集客户 → 批量评分（模块3+4）
5. 为A/B级客户生成个性化触达（模块5）

### 专业版用户

1. 安装 `professional/appliance-export-deal-os/SKILL.md`
2. 拥有基础版全部能力 + 询盘→报价→跟进→谈判→风险全流程

---

## 🎯 核心设计原则

1. **事实与判断分离**：每个结论标注依据
2. **未知标注"未知"**：不编造、不推测
3. **个性化优先**：每个客户独立分析生成
4. **安全分级**：PUBLIC/INTERNAL/RESTRICTED/SECRET 四级数据保护
5. **一次只推进一个目标**：降低客户行动门槛
6. **不完整不报价**：12项检查通过才输出最终报价
7. **下单前必查风险**：29+项风险检查强制通过

## 🔒 数据安全

本体系内置四级数据安全分级：

| 等级 | 标识 | 可否输出到客户 |
|------|:----:|:------------:|
| PUBLIC | 🟢 | ✅ 可以 |
| INTERNAL | 🔵 | ❌ 不可以 |
| RESTRICTED | 🟡 | ❌ 不可以 |
| SECRET | 🔴 | ❌ 绝对不可以 |

详见 `shared/config/security-levels.yaml` 和 `shared/references/security-classification.md`

---

## 🏭 行业知识深度

本体系的差异化竞争力在于**结构化的行业Know-How**：

- **气源匹配**：20+国家/地区的气源类型和压力对照
- **风量标准**：IEC/EN/GB三标准的风量差异（15-25%）
- **油脂分离率**：欧盟ErP法规的特殊要求
- **排风管兼容**：各市场标准尺寸（120/125/150mm）
- **隐性成本**：汇率缓冲/验货费/内陆运费/认证追加等8大利润杀手
- **成交障碍**：7大常见卡单原因诊断器
- **让步交换矩阵**：12种异议×对应交换条件

---

## 📊 用户转化路径

```
免费版 (日均1次评分)
  ↓ 发现每天只能评1个客户不够用
基础版 ¥1,999/年 (无限评分+触达)
  ↓ 客户回复询盘后不知道怎么回复
专业版 ¥5,999/年 (全流程闭环)
  ↓ 团队3+人，需要协作和CRM
企业版 ¥29,800+/年 (私有部署+定制)
```

---

## 📝 版本历史

| 版本 | 日期 | 内容 |
|------|------|------|
| V1.0 MVP | 2026-07 | 基础版：产品定位+客户画像+搜索+评分+触达 |
| V2.0 | 计划中 | 专业版：询盘+报价+跟进+谈判+风险 |
| V3.0 | 计划中 | 企业版：团队+CRM+私有部署+定制知识包 |

---

## ⚠️ 免责声明

本Skill体系提供的分析和建议基于用户输入的信息和行业经验规则，属于**辅助决策工具**。以下事项需要人工专业判断：

- 法律合规和法律风险评估
- 贸易制裁和出口管制合规
- 税务和海关合规
- 银行和付款安全
- 最终商业决策

AI无法替代律师、会计师、报关行和银行的专业意见。

---

## 📧 联系与支持

- 免费版：使用中遇到问题可在评分报告末尾找到帮助入口
- 基础版/专业版：邮箱支持
- 企业版：专属客户成功经理

---

**用50年外贸经验，帮你把每一个客户都开发到极致。**
