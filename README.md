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

### 第一步：填写论文信息

打开 `main.tex`，找到 `\bjutset{ ... }` 块，填写以下字段：

```latex
\bjutset{
  % 论文题目
  ctitle         = {论文中文题目},      % ← 改这里
  etitle         = {English Title},    % ← 改这里

  % 作者信息
  cauthor        = {作者姓名},          % ← 改这里
  studentid      = {S202200001},        % ← 改这里
  cdegree        = {理学硕士},          % ← 按实际选：
                                       %   理学硕士 / 工学硕士 / 管理学硕士
                                       %   理学博士 / 工学博士 / 管理学博士
  cdiscipline    = {学科名称},          % 一级学科，如：物理学 / 机械工程
  cmajor         = {专业方向},          % ← 改这里
  ccollege       = {所在学院},          % ← 改这里

  % 导师信息
  csupervisor    = {导师姓名},          % ← 改这里
  csupervstitle  = {教授},             % 导师职称，如：教授 / 副教授

  % 时间与封面行政信息
  cdate          = {2025年6月},         % ← 改这里
  secretlevel    = {公开},              % 密级：公开 / 限制 / 秘密
  clc            = {O413},             % 中图分类号，在国家图书馆官网查询
  udc            = {530.145},          % UDC 分类号，不确定可留空 {}
}
```

### 第二步：撰写摘要

- `cabstract.tex`：中文摘要正文 + `\ckeywords{关键词一；关键词二；…}`
- `eabstract.tex`：英文摘要正文 + `\ekeywords{keyword one, keyword two, …}`

### 第三步：撰写正文

在 `chapt1.tex` ～ `chapt6.tex` 中按章填写内容。`chapt2.tex` 中保留了常用 LaTeX 元素的示例（公式、表格、图片、定理等），可供参考后删除。

如需**增减章节数**，同步修改 `main.tex` 中的 `\include{...}` 列表：

```latex
\include{chapt1}
\include{chapt2}
% 删除不需要的，或添加 \include{chapt7} 等
```

### 第四步：填写参考文献

在 `references.tex` 的 `thebibliography` 环境中添加条目，或改用 BibTeX（见编译方法）。

### 第五步：填写其余部分

| 文件 | 内容 |
|---|---|
| `appendices.tex` | 附录 |
| `publication.tex` | 攻读学位期间发表论文 |
| `acknowledgement.tex` | 致谢 |
| `notation.tex` | 符号表（可选，不需要则删除 `main.tex` 中对应的 `\include`） |

### 第六步：编译

## 致谢 / Attribution

本模板在 [bjut-swift/BJUTLATEX](https://github.com/bjut-swift/BJUTLATEX)（Apache-2.0）的基础上修改而来，
增加了多章节结构、符号表、附录等框架，以及更完整的编译说明。

## 许可证 / License

[Apache License 2.0](LICENSE)
