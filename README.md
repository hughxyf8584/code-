# EPC AI Lab｜面向国际 EPC 工程管理的 Python 与 AI 实践

这是一个以真实工程管理问题为牵引的个人学习与实践仓库。目标是把 Python、数据分析、工程可视化和 AI 方法逐步转化为可复用、可核验的小工具。

## 项目目标

首个最小可行实践（MVP）是：读取经脱敏或人工构造的周度光伏进度数据，计算计划与实际偏差，按区块和工作项汇总，并生成便于项目团队审阅的表格与图表。

学习顺序：

1. 用 Python 建立可靠的数据读取、清洗和校验流程。
2. 用明确的工程口径计算进度、质量和风险指标。
3. 用图表与报告解释数据，支持管理决策。
4. 再逐步加入 AI：先做有出处的资料检索（RAG），再探索受控的 AI Agent 和 MCP 工具连接。

## 工作原则

- 先明确工程问题、数据口径和验收方式，再写代码。
- 计划值、实际值、偏差及汇总权重都要能追溯；不让 AI 替代关键工程计算。
- AI 输出应引用可核验资料，并由项目责任人确认后用于决策。
- 只使用虚构、脱敏或获准使用的数据。业主文件、合同、报价、员工个人信息和未公开项目数据不得直接提交到公开仓库。
- 先完成一个小而可靠的垂直切片，再添加依赖和功能。

## 当前状态

当前提交只包含工程骨架、学习路线和任务清单，尚未实现进度分析功能。

## 目录结构

~~~text
.
├── README.md
├── pyproject.toml
├── .gitignore
├── data/
│   └── samples/
│       └── README.md
├── docs/
│   └── learning-roadmap.md
├── src/
│   └── epc_ai_lab/
│       └── __init__.py
└── tasks/
    └── initial-backlog.md
~~~

## 环境准备

需要 Python 3.11 或更高版本。仓库采用 src 布局，暂不引入第三方运行时依赖。

~~~bash
python --version
python -m venv .venv
~~~

激活虚拟环境后安装本地包：

~~~bash
# macOS / Linux
source .venv/bin/activate

# Windows PowerShell
.venv\\Scripts\\Activate.ps1

python -m pip install -e .
python -c "import epc_ai_lab; print('EPC AI Lab scaffold ready')"
~~~

## 建议的实践闭环

1. 写清楚需要支持的项目管理问题。
2. 定义数据粒度、字段含义、单位和空值规则。
3. 用小规模合成数据建立确定性的计算基线。
4. 校验计算结果并与工程人员确认口径。
5. 生成图表或报告，检查其是否能支持实际决策。
6. 再评估是否需要 AI、RAG 或 MCP，以及它们的权限和边界。

首批任务与验收条件见 [tasks/initial-backlog.md](tasks/initial-backlog.md)，分阶段学习建议见 [docs/learning-roadmap.md](docs/learning-roadmap.md)。