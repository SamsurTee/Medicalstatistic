# Medical Statistics Interactive Studio

一个面向医学统计教学的静态互动实验站。仓库中的每个模块都是独立 HTML 页面，打开浏览器即可运行，适合课堂演示、学生练习和 GitHub Pages 部署。

Live site: https://samsurtee.github.io/Medicalstatistic/

## 项目定位

这个项目不是单纯的“网页合集”，而是一个可逐步组织课程内容的互动教学入口，重点解决三类问题：

1. 公式会背，但学生很难把参数变化和结果变化联系起来。
2. 检验会算，但不知道该如何解释 P 值、效应量和应用场景。
3. 模块分散，课堂上不容易串成“描述统计 → 分布与抽样 → 推断 → 回归”的完整路径。

因此，仓库现在按“概念表达、统计逻辑、教学应用”三个维度来组织：

- 表达：每个核心模块尽量说明“这个工具解决什么问题”。
- 逻辑：强调指标、方法选择和结论解释之间的关系。
- 应用：加入更接近课堂和医学研究场景的说明与示例。

## 仓库结构

所有交互页都位于仓库根目录，便于 GitHub Pages 直接发布。

| 文件 | 模块主题 | 主要用途 |
|---|---|---|
| `index.html` | 课程入口页 | 统一导航、模块筛选、学习路径说明 |
| `quantitative_descriptive_statistics_single_file_teaching_page.html` | 定量数据统计描述 | 讲均值、中位数、离散程度、异常值和分布形态 |
| `qualitative_stats_interactive.html` | 定性数据统计描述 | 讲率、构成比、RR、OR、标准化率和图形表达 |
| `normal_distribution.html` | 正态分布与尾部概率 | 讲 Z 值、尾部面积、中央区间和临界值 |
| `t_distribution_demo_fixed.html` | t 分布推导 | 讲总体、样本均值、自由度和 t 分布形成过程 |
| `动态置信区间演示.html` | 置信区间 | 讲样本量、标准误和区间宽度变化 |
| `Parameter Estimator_Medical Statistics.html` | 参数估计 | 讲点估计、抽样波动和估计量表现 |
| `chi_square_lab.html` | 卡方检验 | 讲列联表、期望频数、P 值、效应量和结果解释 |
| `mle_logistic_interactive.html` | Logistic 回归 | 讲最大似然、二分类建模和预测概率 |
| `OLS Linear Regression_Interactive Teaching Lab.html` | OLS 线性回归 | 讲拟合、残差和回归系数解释 |

## 推荐教学路径

如果你希望把这些页面作为一门课来使用，建议按下面的顺序安排：

1. 描述统计
   - `quantitative_descriptive_statistics_single_file_teaching_page.html`
   - `qualitative_stats_interactive.html`
2. 分布与抽样
   - `normal_distribution.html`
   - `t_distribution_demo_fixed.html`
3. 参数估计
   - `动态置信区间演示.html`
   - `Parameter Estimator_Medical Statistics.html`
4. 推断与建模
   - `chi_square_lab.html`
   - `mle_logistic_interactive.html`
   - `OLS Linear Regression_Interactive Teaching Lab.html`

这样的顺序有两个好处：

- 学生先建立对数据形态和频率含义的直觉，再进入推断。
- 进入检验和回归时，前面的图形和抽样概念已经打底，不会只剩公式记忆。

## 本地运行

### 方式 1：直接打开

项目中的大部分页面都可以直接双击 `.html` 文件在浏览器中运行。

### 方式 2：使用本地静态服务器

如果你希望测试链接、相对路径和 GitHub Pages 部署效果，可以在仓库目录运行：

```bash
python3 -m http.server 4000
```

然后访问 `http://localhost:4000/`。

### 方式 3：使用 Jekyll

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

## 扩展建议

如果你要继续往里加新实验页，建议遵循下面的约定：

1. 每个新模块保持“单文件即可运行”，避免引入复杂构建流程。
2. 页面顶部写清楚它解释的统计问题，而不是只写工具名称。
3. 页面中至少包含三层信息：
   - 参数输入或数据输入
   - 计算结果或图形结果
   - 解释性文字或应用提示
4. 新页面加入首页目录清单时，补充：
   - 中文标题
   - 英文标题
   - 所属主题
   - 难度层级
   - 关键词和使用场景
5. 如果模块涉及方法选择，尽量把“为什么选这个方法”展示出来，而不是只输出结论。

## 适合继续改进的方向

- 为更多页面补充统一的导航和返回入口。
- 给回归类页面增加医学研究案例模板。
- 为分类资料和连续变量模块增加“课堂练习题 + 标准解释”。
- 把页面中重复使用的样式抽成共享资源文件。

## 基于课程主题仍建议补充的公开信息

在不公开本地课程材料的前提下，站点仍然适合继续补充这些主题：

- 绪论与研究设计导览页
- 医学参考值范围与百分位数解释页
- 假设检验总览与方法选择页
- t 检验选择器或比较页
- 方差分析（ANOVA）互动页
- 相关分析独立页面
- 多元线性回归入门页
- 非参数检验决策页
- 生存分析基础页

这些内容最好采用：

- 合成数据或公开数据
- 通用医学研究场景
- 方法框架、概念图和选择流程

而不是直接复制课堂文件。

## 不宜公开上传的内容

为了避免泄露课程敏感信息，GitHub Pages 上不建议直接放入以下内容：

- 原始课件文件，如 `.key`、`.pptx`、完整讲义 PDF
- 考试、Quiz、翻转课堂题卡、PBL 作业材料
- 真实案例数据、代码本、学生作业或评分相关文件
- 版权受限阅读材料和课程配套 PDF
- 带课程内部痕迹的录屏、视频和案例说明

更安全的做法是：

- 只公开整理后的主题说明
- 使用抽象化案例和脱敏表达
- 把“课程覆盖地图”和“扩展建议”做成独立页面

## English Summary

This repository hosts a browser-only set of interactive teaching labs for medical statistics. Each lab is a standalone HTML page that can be opened locally or deployed directly through GitHub Pages. The project is designed to improve:

- clarity of explanation,
- statistical reasoning,
- classroom usability.

The recommended flow is:

1. descriptive statistics,
2. distributions and sampling,
3. estimation,
4. inference and regression.

If you add new labs, keep them standalone, explain the teaching purpose clearly, and make sure the page includes inputs, outputs, and interpretation.
