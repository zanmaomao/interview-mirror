# Interview Mirror

将面试录音转写稿转化为结构化复盘报告的Skill。输入带有说话人信息的面试文字稿与岗位描述，即可收获一份一份完整的 Markdown 报告，内含逐题分析卡片、四维度综合评估报告与追问预判。

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
| 应聘岗位 + 公司 | 是 |  |
| 岗位 JD | 否 | 提供后额外生成高频题预测 |


---

## 项目结构

```
interview-mirror/
  SKILL.md                    Skill 主文件
  references/
    schema.md                 interview_units.json 字段定义
    question_types.md         题型分类标准与评分维度映射
    output_template.md        Markdown 报告完整模板
```

---



## License

MIT
