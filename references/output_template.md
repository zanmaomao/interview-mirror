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

## 逐题复盘

每道题根据类型使用对应模板。

**普通问答题：**

```markdown
#### Q1：[question]（[primary_label]）

**得分：** X / 5

**考察意图：** [intent]

<details>
<summary>候选人原始回答（点击展开）</summary>

[answer 原文]

</details>

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
#### Q1：[question]（反向提问）

**候选人提问：** [question 原文]

**面试官回答摘要：** [interviewer_response_summary]
```

---

## 预测题

```markdown
---

## 预测题

### 基于本次短板的追问预测
1. **[predicted_question]**（关联 Q[related_unit_id]）
   答题建议：[answer_tip]

### 基于岗位 JD 的高频题（如有）
1. **[question]**（出现 [frequency] 次，来源：[source_label]）
   答题建议：[answer_tip]
```
