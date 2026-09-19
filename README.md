# 2026 华为杯研究生数学建模竞赛 LaTeX 模板

适用于"华为杯"第二十三届中国研究生数学建模竞赛，承办高校为西安交通大学。在已有 GMCMthesis 模板基础上更新，对齐 2026 年官方 Word 模板封面与摘要页。

本仓库是非官方 LaTeX 适配模板。参赛时请以组委会最新要求为准。示例中的学校、成员、队号、摘要与正文需要替换为自己的内容。

## 预览

| 封面 | 摘要页 |
|---|---|
| ![封面](example_1.png) | ![摘要页](example_2.png) |

- [常规示例 PDF](example.pdf)
- [彩色表格示例 PDF](example-color.pdf)

## 编译

安装包含 XeLaTeX、latexmk、BibTeX 和中文支持的 TeX Live 或 MacTeX。在项目根目录执行：

```
latexmk -xelatex -interaction=nonstopmode -halt-on-error example.tex
latexmk -xelatex -interaction=nonstopmode -halt-on-error example-color.tex
```

也可以运行 `bash makefiles.sh`（macOS / Linux）或 `makefiles.bat`（Windows），一次编译两个示例。编译产物为 `example.pdf` 和 `example-color.pdf`。

项目已包含封面、标题所需的 PDF 素材，正常编译无需 Microsoft Word。请保留 `figures/` 目录，并从项目根目录运行编译命令。

### 字体

封面和摘要页固定字形已经嵌入 PDF 素材，包含华文行楷标题。正文根据系统选择字体；Windows 下使用 SimSun（宋体）和 SimHei（黑体），macOS 下使用 Songti SC 和 Heiti SC。

## 填写参赛信息

修改 `example.tex` 或 `example-color.tex` 中的以下字段：

```latex
\title{论文题目}
\baominghao{正式队伍编号}
\schoolname{学校名称}
\membera{成员一}
\memberb{成员二}
\memberc{成员三}
```

随后替换摘要、关键词、正文、参考文献及附录。示例摘要中的格式说明框也应替换为自己的内容。

## 2026 版调整

- 更新第二十三届赛事名称及西安交通大学校徽。
- 从官方 Word 模板提取封面 Logo 和标题 PDF，替换原第二十二届素材。
- 对齐页面尺寸、页边距和页脚位置；正文小四号宋体、论文题目三号黑体、一级标题四号黑体。
- 使用单倍行距，摘要后直接进入正文。
- 封面不显示页码，摘要从 1 开始连续编号。
- 附录代码展示：MATLAB 使用 Courier New 字体，Python 使用 Consolas 字体。

## 格式规范

- 论文题目：三号黑体，居中。
- 一级标题：四号黑体，居中。
- 正文汉字：小四号宋体，单倍行距。
- 页码：从摘要页开始，页脚居中，阿拉伯数字从 1 连续编号。
- 论文不能有页眉，不能有任何可能显示答题人身份的标志。
- 参考文献按正文中的引用次序列出，正文引用处用方括号标示，如 [1][3]。

## 目录

| 文件 | 用途 |
|---|---|
| `example.tex` / `example-color.tex` | 常规 / 彩色表格示例 |
| `gmcmthesis.cls` | 模板类文件 |
| `gmcm.bst` / `reference.bib` | 参考文献样式与示例文献 |
| `figures/` | 封面 Logo、标题 PDF 及示例插图 |
| `makefiles.sh` / `makefiles.bat` | 一键编译脚本 |

## 来源

本项目基于原有 GMCMthesis 模板修改，保留类文件中的 latexstudio.net、andy123t 及相关贡献说明。官方文件及赛事、学校、企业标识的权利归各自权利人所有。

- [中国研究生创新实践系列大赛官网](https://cpipc.chinadegrees.cn)
- [2026 年官方论文格式规范](https://cpipc.chinadegrees.cn)
