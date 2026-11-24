# 课件 Skill · Courseware Slide Design Skill

> 给 AI agent 用的高校课件 PPT 设计系统：视觉规格写死、教学规则写死，产出原生可编辑的 .pptx。

## 它解决什么问题

让 AI 直接做课件 PPT，常见三个毛病：模板味重（五页一个卡片阵列）、文字堆满整页、做出来是图片页没法改。这个 skill 的解法是把设计与教学的决策提前做完、写成硬标准，agent 只负责执行：

- **视觉系统**：白底、主色占 60–70%、强调色每页至多 2 处、禁渐变禁阴影、1pt 细线、统一的标题带母题、12 栏隐形网格。
- **版式菜单**：图主导／数据／对比／流程机理／分类总览／文字页（限量）六种版式，只许从菜单选、相邻页不许同版，每页必须有一个视觉锚点。
- **教学规则**：一页一个概念、正文短语式要点（约 450–520 字/页）、完整句子写进演讲者备注作讲稿、图表在图上直接标注、每页页脚注来源。
- **构建与验收**：先备图片资产包再动手、试点先行、验收拆文件逐页核（字号/字数/备注）＋渲染亲眼看。

## 使用方法

把 `SKILL.md` 放进你的 agent skills 目录（如 Claude Code 的 `~/.claude/skills/courseware-design/`、或任何支持 SKILL.md 格式的 agent 框架），做课件时让 agent 按它执行即可。字号下限、配色 hex、版式菜单都在 SKILL.md 里，可按自己学校的模板改。

## 蒸馏来源与致谢

本 skill 是规则蒸馏，不包含任何来源项目的代码或版式文件：

- [ppt-master](https://github.com/hugohe3/ppt-master)（MIT）— 原生可编辑 PPTX 路线
- [guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill)（AGPL-3.0）— 瑞士国际主义版式纪律（仅借鉴纪律，未使用其代码与版式）
- Anthropic 官方 pptx skill — 配色权重与渲染验收
- [academic-pptx-skill](https://github.com/Gabberflast/academic-pptx-skill)（MIT）— 学术演示内容规则
- course-slides（Genspark genoffice）、deck-studio（teaching-skills）— 教学节奏与无障碍下限
- 第一PPT、WPS 官方课件规范；Mayer 多媒体学习原则

## License

MIT，见 `LICENSE`。
