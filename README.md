# BankAgent Thesis

银行智能助手（BankAgent）毕业设计论文，基于 LaTeX 编写。

## 环境要求

- **编译器**：XeLaTeX（必须，项目使用 `fontspec` 加载 TrueType/系统字体）
- **字体**：Times New Roman（系统自带）
- **发行版**：TeX Live 2024+ 或 MiKTeX

macOS 用户推荐安装 [MacTeX](https://tug.org/mactex/)，Windows 用户推荐 [MiKTeX](https://miktex.org/)。

## 编译

```bash
xelatex main.tex
xelatex main.tex   # 第二次生成目录/交叉引用
```

或者用 `latexmk` 一步到位：

```bash
latexmk -xelatex main.tex
```

编译产出为 `main.pdf`。

## 文件结构

```
.
├── main.tex              # 入口文件，按顺序引入所有章节
├── main_preamble.tex     # 文档类、宏包、字体、间距配置
├── main.pdf              # 编译好的 PDF
├── chapters/
│   ├── front_toc.tex     # 封面/目录
│   ├── abstract.tex      # 摘要
│   ├── declaration.tex   # 声明
│   ├── acknowledgments.tex # 致谢
│   ├── chapter1.tex      # 第1章
│   ├── ...
│   ├── chapter8.tex      # 第8章
│   ├── references.tex    # 参考文献
│   ├── appendix_a.tex    # 附录A
│   ├── appendix_b.tex    # 附录B
│   ├── appendix_c.tex    # 附录C
│   └── contributions.tex # 贡献说明
├── figures/              # 图片资源
└── Final_Project_Report.docx  # Word 版本报告
```

## 协作方式

1. **Clone 仓库**
   ```bash
   git clone git@github.com:dgdgdga/BankAgent_Thesis.git
   cd BankAgent_Thesis
   ```

2. **新建分支写内容**
   ```bash
   git checkout -b your-name/chapterX
   ```

3. **提交时忽略编译中间文件**
   已配置 `.gitignore`（过滤 `.DS_Store`），`main.pdf` **会**被版本管理。如果你不希望提交 PDF，可在 `.gitignore` 中添加 `*.pdf`。

4. **推分支并发起 Pull Request**
   ```bash
   git push -u origin your-name/chapterX
   ```
   然后在 GitHub 页面发起 PR，方便 review 后合并到 `main`。

5. **合并前确认能编译**
   PR 合并前请在本地完整编译一次，确保没有缺包、缺字体或引用错误。

## 注意事项

- `.aux`、`.log`、`.fdb_latexmk`、`.fls` 等中间文件未加入 `.gitignore`（当前全部提交），如需排除可自行添加。
- 字体 `Times New Roman` 在 macOS / Windows 上通常已预装，Linux 需安装 `ttf-mscorefonts` 或用其他 serif 字体替换。
