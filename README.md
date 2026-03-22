# Medical Statistics Interactive Studio

一个面向医学统计教学的静态互动实验站。仓库中的模块均为独立 HTML 页面，浏览器直接打开即可运行，也可以直接部署到 GitHub Pages。

Live site: https://samsurtee.github.io/Medicalstatistic/

## 项目定位

这个仓库现在不只是零散网页合集，而是一个公开安全的医学统计课程入口。它重点解决三类问题：

1. 统计概念听得懂，但参数变化和结果变化之间缺少直觉连接。
2. 会套公式，但不知道该如何选择方法、解释 P 值、效应量和模型系数。
3. 课程主题分散，课堂上不容易串成“研究设计 → 描述统计 → 推断 → 回归 → 生存分析”的完整路径。

因此，仓库按“概念表达、统计逻辑、教学应用、公开边界”四个维度组织：

- 表达：每个页面都尽量先说清楚“这个统计工具解决什么问题”。
- 逻辑：强调变量类型、设计类型、方法选择和结果解释之间的关系。
- 应用：尽量保留适合课堂演示和学生自练的交互环节。
- 边界：只公开合成数据、通用案例和方法框架，不直接上传内部课程文件。

## 当前公开模块

### 课程导览

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `index.html` | 课程入口页 | 统一导航、模块筛选、学习路径说明 |
| `course_coverage_map.html` | 课程覆盖地图 | 说明公开站点已覆盖内容和敏感内容边界 |

### 绪论与研究设计

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `research_design_study_guide.html` | 研究设计导览 | 区分横断面、病例对照、队列、随机对照试验 |

### 描述统计与统计表达

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `quantitative_descriptive_statistics_single_file_teaching_page.html` | 定量数据统计描述 | 讲均值、中位数、离散程度、异常值和分布形态 |
| `qualitative_stats_interactive.html` | 定性数据统计描述 | 讲率、构成比、RR、OR、标准化率和常见图形 |
| `statistical_tables_and_charts_guide.html` | 统计表与统计图 | 讲表格和图形该如何选、如何避免误导 |

### 分布、抽样与参考范围

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `normal_distribution.html` | 正态分布与尾部概率 | 讲 Z 值、尾部面积、中央区间和临界值 |
| `medical_reference_range_lab.html` | 医学参考值范围 | 讲参考范围、百分位数法和正态近似法 |
| `t_distribution_demo_fixed.html` | t 分布推导 | 讲抽样分布、自由度和 t 分布形成过程 |

### 参数估计与假设检验

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `动态置信区间演示.html` | 置信区间 | 讲样本量、标准误和区间宽度变化 |
| `Parameter Estimator_Medical Statistics.html` | 参数估计 | 讲点估计、抽样波动和估计量性质 |
| `hypothesis_testing_roadmap.html` | 假设检验总览 | 讲研究问题、变量类型和检验方法选择 |
| `t_test_lab.html` | t 检验 | 讲单样本、独立样本和配对样本 t 检验 |
| `anova_oneway_lab.html` | 方差分析 | 讲组间变异、组内变异、F 值和 η² |
| `chi_square_lab.html` | 卡方检验 | 讲列联表、期望频数、P 值和效应量 |
| `nonparametric_tests_guide.html` | 非参数检验 | 讲秩和类方法、独立/配对、多组/两组场景选择 |

### 相关与回归建模

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `correlation_analysis_lab.html` | 相关分析 | 讲散点图、Pearson r、Spearman ρ 和离群点影响 |
| `OLS Linear Regression_Interactive Teaching Lab.html` | OLS 线性回归 | 讲拟合、残差和回归系数解释 |
| `multiple_linear_regression_lab.html` | 多元线性回归 | 讲控制变量、偏回归系数、调整 R² 和共线性 |
| `mle_logistic_interactive.html` | Logistic 回归 | 讲最大似然、二分类建模和预测概率 |

### 时间结局分析

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `survival_analysis_explorer.html` | 生存分析 | 讲 Kaplan-Meier 曲线、删失、log-rank 和中位生存时间 |

## 本轮补齐的公开模块

这次已经补齐以下公开安全页面：

- 研究设计导览
- 医学参考值范围实验页
- 统计表与统计图指南
- 假设检验总览
- t 检验实验页
- 单因素 ANOVA 实验页
- 相关分析实验页
- 多元线性回归实验页
- 非参数检验选择页
- 生存分析基础实验页

这些页面都只使用：

- 合成数据
- 通用医学研究场景
- 方法框架和解释逻辑

不会直接暴露本地课程文件内容。

## 推荐教学路径

如果你希望把这些页面作为一门课来使用，建议按下面的顺序安排：

1. 研究问题与设计
   - `research_design_study_guide.html`
2. 描述统计与表达
   - `quantitative_descriptive_statistics_single_file_teaching_page.html`
   - `qualitative_stats_interactive.html`
   - `statistical_tables_and_charts_guide.html`
3. 分布、抽样与参考范围
   - `normal_distribution.html`
   - `medical_reference_range_lab.html`
   - `t_distribution_demo_fixed.html`
4. 参数估计与假设检验
   - `动态置信区间演示.html`
   - `Parameter Estimator_Medical Statistics.html`
   - `hypothesis_testing_roadmap.html`
   - `t_test_lab.html`
   - `anova_oneway_lab.html`
   - `chi_square_lab.html`
   - `nonparametric_tests_guide.html`
5. 相关与回归
   - `correlation_analysis_lab.html`
   - `OLS Linear Regression_Interactive Teaching Lab.html`
   - `multiple_linear_regression_lab.html`
   - `mle_logistic_interactive.html`
6. 时间结局
   - `survival_analysis_explorer.html`

这样的路径有两个直接好处：

- 学生会先建立研究设计和变量类型的框架，再进入具体计算。
- 后续讲回归、生存分析时，前面的描述统计、抽样误差和检验逻辑已经打底。

## 本地运行

### 方式 1：直接打开

项目中的大部分页面都可以直接双击 `.html` 文件在浏览器中运行。

### 方式 2：本地静态服务器

如果你希望测试链接、相对路径和 GitHub Pages 效果，可以在仓库目录运行：

```bash
python3 -m http.server 4000
```

然后访问 `http://localhost:4000/`。

### 方式 3：Jekyll

仓库保留了 GitHub Pages/Jekyll 配置，适合与线上部署保持一致：

```bash
bundle install
bundle exec jekyll serve --livereload
```

默认地址为 `http://localhost:4000`。

## 部署

仓库可以直接部署到 GitHub Pages：

- 发布分支：`main`
- 首页入口：`index.html`
- 站点地址：https://samsurtee.github.io/Medicalstatistic/

## 公开安全边界

为了避免泄露课程敏感信息，GitHub Pages 上不建议直接放入以下内容：

- 原始课件文件，如 `.key`、`.pptx`、完整讲义 PDF
- 考试、Quiz、翻转课堂题卡、PBL 作业材料
- 真实病例数据、代码本、学生作业或评分相关文件
- 带课程内部说明的录屏、视频和案例资料
- 版权受限阅读材料和课程配套 PDF

更安全的做法是：

- 只公开整理后的主题说明
- 使用抽象化案例和脱敏表达
- 用合成数据演示方法逻辑
- 把课程覆盖范围和公开边界做成独立页面说明

## 后续适合继续精修的方向

在不公开敏感材料的前提下，后续更适合继续做这些改进：

- 统一更多页面的组件、配色和导航体验
- 给核心模块补充“课堂练习题 + 标准解释”
- 增加统计术语索引和方法选择速查页
- 把重复样式和脚本逐步抽成共享资源

## English Summary

This repository is now a public-safe course portal for medical statistics, not just a collection of static pages. It covers:

1. study design,
2. descriptive statistics,
3. distributions and reference ranges,
4. estimation and hypothesis testing,
5. correlation and regression,
6. survival analysis.

All pages are standalone HTML files designed for browser-only use and GitHub Pages deployment. Public pages use synthetic data, generic teaching scenarios, and method logic only. Internal course files, quizzes, slides, PDFs, videos, and real datasets should remain private.
