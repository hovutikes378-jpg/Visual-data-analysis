# Titanic 数据可视化分析

基于 D3.js 的 Titanic 数据集可视化项目，支持交互式数据探索。

## 在线访问

- GitHub Pages: `https://[你的用户名].github.io/Visual-data-analysis/`
- Vercel 备用部署

## 项目结构

```
├── index.html          # 主页面（包含全部 CSS/JS/D3.js 可视化）
├── data/
│   └── titanic.csv     # Titanic 数据集
└── README.md
```

## 可视化内容

1. **按性别分组生存率** — 展示男性和女性的幸存/遇难人数对比及生存率
2. **按年龄分组生存率** — 按儿童(0-12)、青少年(13-17)、青年(18-30)、中年(31-50)、中老年(51-65)、老年(66+)分组展示生存率
3. **年龄分布直方图** — 展示不同年龄段乘客数量，支持切换按生存状态叠放显示
4. **票价分布直方图** — 展示票价分布情况，支持切换按生存状态叠放显示

## 交互功能

- **悬停显示详情**：鼠标移到图表上即可查看具体数据
- **视图切换**：年龄分布和票价分布支持"乘客数量"和"按生存状态"两种视图模式切换

## 部署指南

### GitHub Pages 部署

```bash
# 1. 创建 GitHub 仓库（命名为 Visual-data-analysis）
# 2. 在本地初始化并推送
git init
git add .
git commit -m "Initial commit: Titanic D3.js visualization"

# 3. 推送到 GitHub
git remote add origin https://github.com/[你的用户名]/Visual-data-analysis.git
git branch -M main
git push -u origin main

# 4. 创建并推送到 gh-pages 分支
git checkout -b gh-pages
git push origin gh-pages

# 5. 在 GitHub 仓库 Settings → Pages 中：
#    - Source: Deploy from a branch
#    - Branch: gh-pages, / (root)
#    - 访问：https://[你的用户名].github.io/Visual-data-analysis/
```

### Vercel 部署

1. 登录 [Vercel](https://vercel.com)
2. Import 你的 GitHub 仓库 `Visual-data-analysis`
3. Framework Preset 选择 `Other`
4. 部署后即可获得访问链接

## 技术栈

- **D3.js v7** — 数据驱动文档，核心可视化库
- **HTML5 + CSS3** — 响应式页面布局
- **Titanic Dataset** — 来自 [datasciencedojo/datasets](https://github.com/datasciencedojo/datasets)

## 数据集说明

Titanic 数据集包含 891 名乘客的信息，12 个字段：
- `Survived`: 是否幸存（0=遇难, 1=幸存）
- `Pclass`: 船舱等级（1/2/3）
- `Sex`: 性别
- `Age`: 年龄
- `SibSp/Parch`: 家庭关系
- `Fare`: 票价
- `Embarked`: 登船港口
- 等
