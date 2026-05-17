# 北京工业大学学位论文 LaTeX 模板

> ⚠️ **非官方模板**：本项目由个人维护，与北京工业大学官方无关，不代表学校立场。使用前请以[北工大研究生院发布的最新撰写规范](https://graduate.bjut.edu.cn/beijinggongyedaxueyanjiushengxueweilunwenzhuanxieguifan.pdf)为准，并向导师或院系确认格式要求。

从北工大学位论文中剥离具体内容后得到的纯模板，支持学术学位硕士、专业学位硕士、学术学位博士、专业学位博士四种封面，保留排版结构、字体、Logo、宏包配置及各章节框架。

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
├── chapt1.tex ~ chapt5.tex  # 正文各章节（第5章为结论与展望）
├── notation.tex          # 符号表（物理量名称及符号表，可选）
├── appendices.tex        # 附录
├── references.tex        # 参考文献（thebibliography 环境）
├── reference.bib         # 可选：BibTeX 数据库
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

如需生成**索引**（博士论文常用，硕士一般省略）：

```bash
xelatex main
makeindex main
xelatex main
xelatex main
```

如不需要索引，在 `main.tex` 中注释掉 `\usepackage{makeidx}`、`\makeindex` 和 `\printindex` 三行即可。

## 使用步骤

### 第一步：填写论文信息

打开 `main.tex`，找到 `\bjutset{ ... }` 块，填写以下字段：

```latex
\bjutset{
  % 封面类型（决定封面底色，四选一）
  covertype      = {academic-master},   % 见下方"封面颜色对照"

  % 论文题目
  ctitle         = {论文中文题目},      % ← 改这里（≤ 25 字，不设副标题）
  etitle         = {English Title},    % ← 改这里（字母全部大写）

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
  （硕士 500～1000 字，博士 1000～2000 字；关键词 3～5 个，由外延大到小排列）
- `eabstract.tex`：英文摘要正文 + `\ekeywords{keyword one, keyword two, …}`
  （约 300 个实词，内容与中文摘要对应）

### 第三步：撰写正文

在 `chapt1.tex` ～ `chapt5.tex` 中按章填写内容。`chapt2.tex` 中保留了常用 LaTeX 元素的示例（公式、表格、图片、定理等），可供参考后删除。第5章（`chapt5.tex`）为结论与展望。

如需**增减章节数**，在 `main.tex` 中同步修改 `\include{...}` 列表：

```latex
\include{chapt1}
\include{chapt2}
\include{chapt3}
\include{chapt4}
% 如需增加，在此添加 \include{chapt6} 等，并将结论移至最后
\include{chapt5}   % 结论与展望（保持在最后）
```

### 第四步：填写参考文献

在 `references.tex` 的 `thebibliography` 环境中添加条目，或改用 BibTeX（见编译方法）。

### 第五步：填写其余部分

| 文件 | 内容 |
|---|---|
| `notation.tex` | 符号表（可选，不需要则注释掉 `main.tex` 中的 `\include{notation}`） |
| `appendices.tex` | 附录 |
| `publication.tex` | 攻读学位期间发表论文 |
| `acknowledgement.tex` | 致谢 |

### 第六步：编译

## 封面颜色对照

> **提示**：封面（含彩色皮壳、烫金字等）通常由打印店按学校要求统一制作，无需自行打印。提交电子版或内文打印时可忽略封面颜色是否精确，交给打印店处理即可。

在 `main.tex` 的 `covertype` 字段选择对应值：

| covertype | 适用人群 | 封面底色 |
|---|---|---|
| `academic-master` | 全日制学术学位硕士 / 同等学力硕士 | 蓝色 #177CB2 |
| `professional-master` | 全日制/非全日制专业学位硕士 | 青绿色 #009C86 |
| `academic-doctor` | 学术学位博士 | 深红色 #931E31 |
| `professional-doctor` | 专业学位博士 | 橙色 #DE5F12 |

## 北工大规范要点速查

以下要点摘自[《北京工业大学研究生学位论文撰写规范》](https://graduate.bjut.edu.cn/beijinggongyedaxueyanjiushengxueweilunwenzhuanxieguifan.pdf)，填写时请注意：

| 项目 | 硕士要求 | 博士要求 |
|---|---|---|
| **中文题目** | ≤ 25 字，不设副标题 | 同左 |
| **英文题目** | 字母全部大写 | 同左 |
| **中文摘要字数** | 500～1000 字 | 1000～2000 字 |
| **英文摘要** | 实词约 300 个 | 同左 |
| **关键词数量** | 3～5 个，由大到小排列 | 同左 |
| **参考文献总数** | ≥ 40 篇 | ≥ 100 篇 |
| **其中外文文献** | ≥ 20 篇 | ≥ 总数的 1/2 |
| **近五年文献** | ≥ 总数的 1/3 | 同左 |

其他注意事项：
- 每章末尾须设「**本章小结**」小节（已在模板各章中预留）。
- 摘要中不使用公式、图表，不标注文献编号。
- 图表题注：图题置于图下方，表题置于表上方，采用三线表。
- 公式按章编号，如（1-1）、（2-3）（模板已配置中文圆括号格式）。

## 致谢 / Attribution

本模板在 [bjut-swift/BJUTLATEX](https://github.com/bjut-swift/BJUTLATEX)（Apache-2.0）的基础上修改而来，
增加了多章节结构、符号表、附录等框架，封面颜色自动匹配学位类型，以及更完整的编译说明。

## 许可证 / License

[Apache License 2.0](LICENSE)
