# LaTeX 使用教程扩展版

## 1. 文本格式

### 常见文本格式操作

| 功能     | 命令                                      | 示例                        |
| -------- | ----------------------------------------- | --------------------------- |
| 加粗     | `\textbf{text}`                           | `\textbf{加粗文字}`         |
| 斜体     | `\textit{text}`                           | `\textit{斜体文字}`         |
| 下划线   | `\underline{text}`                        | `\underline{下划线}`        |
| 删除线   | `\sout{text}`（需 `ulem` 包）             | `\sout{删除线}`             |
| 字体大小 | `\tiny, \small, \large`                   | `{\large 大字体}`           |
| 居中     | `\begin{center} ... \end{center}`         | `居中内容`                  |
| 颜色     | `\textcolor{red}{text}`（需 `xcolor` 包） | `\textcolor{red}{红色文字}` |

### 示例代码

```latex
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{ulem} % 删除线
\usepackage{xcolor} % 颜色支持
\begin{document}

\textbf{加粗文字} \\
\textit{斜体文字} \\
\underline{下划线} \\
\sout{删除线} \\
{\large 大字体文字} \\
\textcolor{blue}{蓝色文字} \\

\begin{center}
这是居中的内容
\end{center}

\end{document}
```

---

## 2. 数学公式

### 行内公式

使用 `$...$` 包裹公式：

```latex
公式示例：$E=mc^2$
```


### 独立公式

使用 `\[...\]` 创建独立公式：

```latex
\[
a^2 + b^2 = c^2
\]
```

### 常见数学符号

| 符号 | 命令          | 示例                            |
| ---- | ------------- | ------------------------------- |
| 分数 | `\frac{a}{b}` | \(\frac{a}{b}\)                 |
| 求和 | `\sum`        | \(\sum_{i=1}^n i\)              |
| 积分 | `\int`        | \(\int_{a}^{b} x \,dx\)         |
| 根号 | `\sqrt{x}`    | \(\sqrt{x}\)                    |
| 上标 | `x^n`         | \(x^n\)                         |
| 下标 | `x_n`         | \(x_n\)                         |

### 示例代码

```latex
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{amsmath}
\begin{document}

行内公式示例：$E=mc^2$ \\

独立公式示例：
\[
a^2 + b^2 = c^2
\]

一些常见符号：
\[
\frac{a}{b}, \quad \sum_{i=1}^n i, \quad \int_a^b x \,dx, \quad \sqrt{x}, \quad x^n, \quad x_n
\]

\end{document}
```

---

## 3. 表格

### 基本表格

LaTeX 代码：

```latex
\begin{tabular}{|c|c|c|}
\hline
A & B & C \\
\hline
1 & 2 & 3 \\
4 & 5 & 6 \\
\hline
\end{tabular}
```

效果：

| A | B | C |
|---|---|---|
| 1 | 2 | 3 |
| 4 | 5 | 6 |

### 高级表格示例

LaTeX 代码：

```latex
\begin{tabular}{|l|r|c|}
\hline
左对齐 & 右对齐 & 居中对齐 \\
\hline
Apple  & 3.50   & Yes \\
Banana & 1.20   & No  \\
Cherry & 2.00   & Yes \\
\hline
\end{tabular}
```

效果：

| 左对齐 | 右对齐 | 居中对齐 |
| ------ | ------ | -------- |
| Apple  |   3.50 | Yes      |
| Banana |   1.20 | No       |
| Cherry |   2.00 | Yes      |

---

## 4. 插入图片

### 示例代码

```latex
\usepackage{graphicx} % 加载图片功能包
\begin{figure}[h]
\centering
\includegraphics[width=0.5\textwidth]{example.png} % 指定图片宽度
\caption{图片示例}
\end{figure}
```

### 注意事项

- 图片文件（如 `example.png`）需上传到 Overleaf 项目中。
- `width=0.5\textwidth` 控制图片宽度为页面宽度的一半。

---

## 5. 引用和参考文献

### 示例代码

```latex
\usepackage{cite}
本文参考文献见~\cite{example}。

\begin{thebibliography}{99}
\bibitem{example} 作者姓名, 文章标题, 期刊名, 年份.
\end{thebibliography}
```

---

## 6. Overleaf 高级功能

### 1. 使用模板

- 点击 “New Project” > “Template Gallery”。
- 在搜索栏输入关键词（如 "CV", "Thesis"）找到合适模板。
- 打开模板后可直接修改内容。

### 2. 多人协作

- 点击页面右上角的 “Share” 按钮。
- 生成分享链接或邀请协作者。

### 3. 版本控制

- 点击 “History & Revisions” 查看历史版本。
- 支持回滚到指定版本。

---

## 7. 常见问题及解决方法

### 1. 中文支持问题

加载中文字体包：

```latex
\usepackage{ctex}
```

### 2. 编译错误

- 检查是否漏掉了 `}` 或 `\end`。
- 按错误提示逐一修正。

### 3. 导出 PDF

- 点击页面顶部的 “Download PDF”。
