# 报告输出模板

报告文件名：`面试复盘_[岗位]_[日期].md`（如 `面试复盘_产品经理_20260422.md`）

---

## 报告头部

公司名、面试轮次若未提供则渲染为"未提供"。

```markdown
# 面试复盘报告
[公司名或"未提供"] · [岗位名]
[面试轮次或"未提供"] · [日期]
综合评分 X.X / 5
```

---

## 总览部分

```markdown
---

## 总览

### 一句话总结
[overall_summary]

### 维度评分

| 维度 | 评分 | 简评 |
| --- | --- | --- |
| 结构化与逻辑 | X.X/5 | [dim_structure 摘要] |
| 经验与量化结果 | X.X/5 | [dim_quantification 摘要] |
| 业务/专业认知 | X.X/5 或 - | [dim_business 摘要，若未涉及填"本次未涉及"] |
| 沟通与自我呈现 | X.X/5 | [dim_self_presentation 摘要] |

### 核心竞争力
- [优势1]
- [优势2]

### 致命扣分项
- [短板1]（Q2、Q5）：[对岗位的负面影响]
- [短板2]（Q3）：[对岗位的负面影响]
```

---

## 逐题复盘

每道题根据类型使用对应模板。

**普通问答题：**

```markdown
#### Q1：[question_summary]（[primary_label]）

**得分：** X / 5
**考察意图：** [intent]
**候选人回答：** [answer 原文]
**回答摘要：** [answer_summary]
**优点：**
- [strength1]
- [strength2]
**不足：**
- [weakness1]
- [weakness2]
**建议：** [suggestion]
**优化参考回答：** [optimized_answer]
```

**反向提问（is_candidate_question = true）：**

```markdown
#### Q1：[question_summary]（反向提问）

**候选人提问：** [question 原文]
**面试官回答摘要：** [interviewer_response_summary]
```

---

## 预测题与下一步行动

```markdown
---

## 预测题

### 基于本次短板的追问预测
1. **[predicted_question]**（关联 Q[related_unit_id]）
   答题建议：[answer_tip]

### 基于岗位 JD 的高频题（如有）
1. **[question]**（出现 [frequency] 次，来源：[source_label]）
   答题建议：[answer_tip]

---

## 下一步行动

1. **[problem]**（Q[related_units]）：[action]
2. **[problem]**（Q[related_units]）：[action]
```
