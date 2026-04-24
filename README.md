# Interview Mirror 🥰

将面试录音转写稿转化为结构化复盘报告的 Skill。输入带有说话人信息的面试文字稿与岗位描述，即可收获一份完整的 Markdown 报告，内含逐题分析卡片与追问预判。

---

## 快速开始


```bash

# 下载
npx skills add zanmaomao/interview-mirror

# 更新
npx skills update interview-mirror

```

---

## 输入要求

| 输入项 | 必填 | 说明 |
| --- | --- | --- |
| 面试文字稿 | 是 | 粘贴文本，或提供 .txt / .md / .docx 文件路径；使用录音转文字软件导出时建议保留说话人，时间戳无需保留 |
| 应聘岗位 | 是 |  |
| 公司名称 | 否 | 提供后搜索真实面经，未提供时高频题预测仅基于 JD 推断 |
| 岗位 JD | 否 | 提供后额外生成高频题预测 |


---

## 项目结构

```
interview-mirror/
  SKILL.md                    Skill 主文件
  references/
    schema.md                 interview_units.json 字段定义
    question_types.md         题型分类标准与优化思路
    output_template.md        DIY你的 Markdown 报告完整模板
    scoring_rubric.md         DIY你的评分标准
```

---

在线网站（仍在优化，功能和标准尚未对其到skill）：
- https://interviewcompass.top

---

## License

MIT
