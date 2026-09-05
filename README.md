# bigdata-ai-coursework

> 《大数据与人工智能》课程作业仓库-黄诗雨

本仓库用于存放课程的全部作业、实验代码与学习笔记，按「作业编号」组织，每次作业一个独立子目录，保证过程可追溯、结果可复现。

## 目录结构

```
bigdata-ai-coursework/
├── README.md              # 仓库说明（本文件）
├── requirements.txt       # Python 依赖清单
├── assignments/           # 课程作业（核心目录）
│   ├── README.md          # 作业索引与进度表
│   └── hw01-xxx/          # 单次作业：代码 + 报告 + 数据说明
├── notebooks/             # Jupyter 实验与探索性分析
├── src/                   # 可复用的通用代码 / 工具函数
├── data/                  # 数据文件（默认不入库，见 .gitignore）
└── docs/                  # 课程资料、环境配置笔记
```

## 环境准备

```bash
# 1. 创建虚拟环境（推荐，避免污染全局 Python）
python -m venv .venv

# 2. 激活虚拟环境
# Windows (Git Bash):
source .venv/Scripts/activate
# Windows (PowerShell):
.venv\Scripts\Activate.ps1
# macOS / Linux:
source .venv/bin/activate

# 3. 安装依赖
pip install -r requirements.txt
```

## 作业提交规范

| 项目 | 约定 |
| --- | --- |
| 目录命名 | `hw<编号>-<简短主题>`，如 `hw02-decision-tree` |
| 每次作业 | 至少包含 `README.md`（题目 + 思路 + 结论）与源码 |
| 提交信息 | `hw01: 完成数据清洗与描述性统计` |
| 数据文件 | 大文件（>50MB）不入库，在作业 README 中注明来源与下载方式 |

## 提交信息约定

采用 `<范围>: <动作>` 的格式，保持历史记录清晰：

```
hw01: 完成数据清洗与描述性统计
hw02: 新增决策树分类实验
docs: 补充 PySpark 环境配置说明
fix: 修正缺失值填充逻辑
```

## 常用命令速查

```bash
git status              # 查看当前改动
git add .               # 暂存全部改动
git commit -m "hw01: 说明"   # 提交
git push                # 推送到 GitHub
git pull                # 拉取远程最新内容
git log --oneline       # 查看提交历史
```

---

_持续更新中 · 2026 秋_

## 作业1：概念学习资料生成项目
### 仓库用途
本仓库存放概念学习资料生成项目级 Skill，自动生成 AI 概念学习网页。

### Skill 存放路径
`.workbuddy/skills/concept-learning-generator/SKILL.md`

### WorkBuddy 调用示例
```
@concept-learning-generator
concept_name="Agent"
```
### 已产出学习资料
Agent、大模型上下文窗口、Skill 三份 html
## 人工核查与修改记录
1. 对SKILL.md的结构进行核对，确认YAML元数据、适用场景、输入参数、执行步骤、输出结构、资料规范、自检规则完整齐全，保证Skill支持任意新概念输入，不是一次性提示词。
2. 对三份生成HTML学习资料人工校验：确认5个章节完整；逐个打开参考链接，确保链接真实可访问；修正AI生成的部分表述，补充个人理解解释，区分官方定义和个人解读。
3. 核对concept‑relationship.md，确认讲清Agent、大模型上下文、Skill三者关系，重点确认上下文如何影响Agent运行、Skill如何沉淀复用任务知识。
4. Git提交前检查仓库，确认没有上传密钥、隐私信息，使用.gitignore排除敏感文件。
# AI概念学习资料仓库
作业1：用AI构建个人概念学习资料生成Skill

## 仓库文件结构
- workbuddy/skill.md：项目级Skill定义文件
- learning‑materials/：三份HTML概念学习资料
  - agent.html：Agent概念学习页面
  - llm‑context.html：LLM上下文概念学习页面
  - skill.html：Skill概念学习页面
- concept‑relationship.md：Agent、LLM上下文、Skill三者概念关系说明
- README.md：项目说明文档

## 项目说明
本仓库使用Skill生成三份AI概念学习网页，每份学习资料包含个人解释、机制、应用场景、学习目标、核心问题、自测问题。
