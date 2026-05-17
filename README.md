# 北京工业大学碩士学位论文 LaTeX 模板

从一份完整的北工大学位论文中剥离具体内容后得到的纯模板，保留排版结构、字体、Logo、宏包配置及各章节框架。

## 环境要求

| 工具 | 说明 |
|---|---|
| **TeX 发行版** | TeX Live 2020+（推荐）、MacTeX 2020+、MiKTeX |
| **编译引擎** | **XeLaTeX**（必须，用于中文字体支持） |
| **所需宏包** | ctex、amsmath、booktabs、graphicx、hyperref、cleveref 等（均包含在 TeX Live 完整安装中） |

### 安装 TeX 发行版

**macOS**
```bash
# 推荐：MacTeX（约 5 GB，包含全部宏包，开箱即用）
brew install --cask mactex

# 或从官网下载：https://tug.org/mactex/
```

**Windows**
下载并安装 [TeX Live](https://tug.org/texlive/)（选 full scheme）或 [MiKTeX](https://miktex.org/download)。

**Linux**
```bash
# Ubuntu / Debian
sudo apt install texlive-full texlive-lang-chinese

# Arch
sudo pacman -S texlive-most
```

**Overleaf**（无需本地安装）：新建项目 → 上传全部文件 → 编译器改为 **XeLaTeX** → 编译即可。

> **字体说明**：模板目录中已附带 `SimSun.ttc`、`SimHei.ttf`、`FangSong.ttf`、`Kaiti.ttf` 四个字体文件，无需额外安装系统字体，在所有平台（含 Overleaf）上均可直接使用。

## 目录结构

```
bjut_thesis_template/
├── main.tex              # 主文件，包含论文信息和各章节 \include
├── bjutthesis.cls        # 论文类文件（请勿随意修改）
├── bitoc.sty             # 中英双语目录支持
├── ezinfo.sty / .cfg     # 辅助配置
├── cleveref.cfg          # 引用名配置
├── gbref.bst             # 国标参考文献样式
├── cabstract.tex         # 中文摘要
├── eabstract.tex         # 英文摘要
├── chapt1.tex ~ chapt6.tex  # 正文各章节
├── appendices.tex        # 附录
├── references.tex        # 参考文献（thebibliography 环境）
├── reference.bib         # 可选：BibTeX 数据库
├── notation.tex          # 可选：符号表
├── publication.tex       # 攻读学位期间发表论文
├── acknowledgement.tex   # 致谢
├── SimSun.ttc / SimHei.ttf / FangSong.ttf / Kaiti.ttf   # 字体
└── bjut_logo_color.pdf / bjut_logo_white.pdf            # 校徽
```

## 编译方法

需使用 **XeLaTeX** 引擎编译（因为模板使用 ctex/中文字体）：

```bash
xelatex main
xelatex main      # 第二次以正确生成目录、交叉引用
```

如使用 BibTeX 管理参考文献：

```bash
xelatex main
bibtex  main
xelatex main
xelatex main
```

## 使用步骤

1. 打开 `main.tex`，在 `\bjutset{ ... }` 中填入题目、作者、导师、学号、日期等信息。
2. 在 `cabstract.tex` / `eabstract.tex` 中撰写中英文摘要与关键词。
3. 在 `chapt1.tex` ~ `chapt6.tex` 中撰写正文各章节。如需增减章节，
   请同步修改 `main.tex` 中的 `\include{...}` 列表。
4. 在 `references.tex` 中添加参考文献条目。
5. 在 `appendices.tex` / `publication.tex` / `acknowledgement.tex` 中
   填写附录、发表论文与致谢。
6. 使用 XeLaTeX 编译。

## 致谢 / Attribution

本模板在 [bjut-swift/BJUTLATEX](https://github.com/bjut-swift/BJUTLATEX)（Apache-2.0）的基础上修改而来，
增加了多章节结构、符号表、附录等框架，以及更完整的编译说明。

## 许可证 / License

[Apache License 2.0](LICENSE)
