# ml-lab-classic

经典机器学习算法实践：糖尿病回归（线性回归 / 随机森林 / XGBoost）与威斯康星乳腺癌逻辑回归。

## 绑定 Cursor 工作区

1. 菜单 **File → Open Folder…**（或 **文件 → 打开文件夹**），选择 `D:\Project\ml-lab-classic`。
2. 或在欢迎页 **Open project**，指向同一文件夹。

之后终端默认目录、搜索与 AI 上下文都会以该文件夹为根目录。

## 使用 Anaconda 环境（推荐）

在 **Anaconda Prompt** 或已初始化 conda 的 PowerShell 中执行：

```bash
cd D:\Project\ml-lab-classic
conda create -n ml-lab-classic python=3.11 -y
conda activate ml-lab-classic
pip install -r requirements.txt
```

可选：用 conda 安装部分包（版本由 conda-forge 决定）：

```bash
conda install -n ml-lab-classic -c conda-forge numpy pandas scikit-learn matplotlib seaborn jupyter -y
pip install xgboost
```

运行 Jupyter：

```bash
conda activate ml-lab-classic
jupyter lab
```

打开 `notebooks/01_diabetes_regression.ipynb` 与 `notebooks/02_breast_cancer_logistic.ipynb`，**Run All** 即可复现。

## GitHub 实时上传

```bash
cd D:\Project\ml-lab-classic
git init
git add .
git commit -m "chore: initial ml-lab-classic"
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git branch -M main
git push -u origin main
```

之后每次修改：`git add -A && git commit -m "说明" && git push`。

## 关于 Cursor 里的 Plan / Build

- **Plan**：把任务拆成步骤的检查清单（做什么、顺序如何），**不等于已执行的代码**。
- **Build / 按 Plan 执行**：表示按该计划在仓库里真正创建文件、环境与脚本；本仓库中的 `notebooks/`、`requirements.txt`、`.gitignore` 即对应计划落地结果。

若本机尚未执行 `conda create`，需你本地在 Anaconda 里运行上面的 conda 命令（AI 无法代替你在你电脑上安装 Anaconda）。

## 中文字体（Windows）

Notebook 已优先使用 `Microsoft YaHei`；若图表中文仍异常，可将 `font.sans-serif` 改为本机已安装的中文字体名。
