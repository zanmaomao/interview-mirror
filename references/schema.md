# 文件格式

> 以下所有文件仅在 P2.5 判定为**分批路径**时由主 agent 写入工作目录；标准路径（< 10000 字）下，P1/P2 结果只保留在上下文中，不写盘。

## interview_speaker_mapping.json

分批路径：P2.5 写入工作目录，供子 agent 读取说话人角色映射。

```json
{
  "interviewer": ["S1"],
  "candidate": "S2",
  "confidence": "high"
}
```

## interview_units.json

分批路径：P2.5 写入工作目录的完整单元列表，保留候选人回答原文和所有 P2 字段。

```
[
  {
    unit_id,             // 题目编号，从1开始连续
    is_followup,         // 是否为追问题
    parent_unit_id,      // 追问题指向的主问题 unit_id，否则为 null
    has_followups,       // 该题是否被追问过（P4a 依据此字段）
    is_candidate_question,
    question,            // 完整提问文本（含所有子问题）；反向提问时为候选人提问原文
    answer,              // 候选人完整回答原文；反向提问时为 null
    interviewer_response_summary  // 仅反向提问（is_candidate_question = true）时：面试官回答摘要
  }
]
```

## 超长文字稿分批文件格式

主 agent 复用 `interview_speaker_mapping.json` 和 `interview_units.json`，生成供子 agent 读取的分批 JSON 文件。

**batch_N.json**
```json
{
  "batch_id": 1,
  "units": [ /* 该批次的问答单元列表，含完整原文和所有 P2 字段 */ ],
  "cross_batch_parent_questions": [
    /* 若本批次中有追问题的父题在上一批次，将父题 question 和 answer 原文补入此处 */
    { "unit_id": 3, "question": "...", "answer": "..." }
  ]
}
```

**batch_N_result.json**（子 agent 输出）
```json
{
  "batch_id": 1,
  "units": [
    {
      "unit_id": 1,
      "primary_label": "行为类",
      "secondary_label": null,
      "intent": "...",
      "answer_summary": "...",
      "score": 3,
      "strength": ["..."],
      "weakness": ["..."],
      "suggestion": "...",
      "expression_note": null,
      "optimized_answer": "..."
    }
  ]
}
```

`batch_N_result.json` 中每个单元除用于匹配回填的 `unit_id` 外，只包含 P3 分析字段，不包含 `question`、`answer`、`interviewer_response_summary` 或其他 P2 字段。P5 写最终报告时，「候选人回答」字段从 `interview_units.json` 按 `unit_id` 重新提取。
