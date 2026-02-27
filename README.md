# 📄 高级中文 LaTeX 简历模板 (IT/算法/工程向)

这是一个排版紧凑、专业且极简的中文简历 LaTeX 模板。默认采用 10.5pt 字号（五号字）与经典的科技蓝配色，极其适合 **算法工程师、大模型开发、软件开发及各类 IT 互联网行业** 的求职者。

模板原生支持**全局背景水印**与**照片排版**，完美适配**在线 LaTeX 编辑器（[LoongTex](https://app.loongtex.com)）**，支持快速编译与 PDF 高清生成，开箱即用。

---

## 📸 示例预览

[![简历预览](./demo/template.png)](./demo/TEMPLATE.pdf)

👉 **[点击此处查看高清 PDF 示例](./demo/TEMPLATE.pdf)**

---

## 📂 文件结构

```text
.
├── template.tex              # 主 LaTeX 模板文件（在此处编写你的简历内容）
├── images/                   # 图片资源文件夹
│   ├── template_avatar.png   # 示例头像图片（推荐使用 1:1 或接近正方形的比例）
│   └── template_logo.png     # 页面背景水印图片（透明度已在代码中默认设为 10%）
└── demo/                     # 预览示例文件夹
    ├── template.png          # 编译后的简历预览长图
    └── template.pdf          # 编译后的简历 PDF 文件

```

---

## 🛠️ 使用指南

### 推荐方式：在线编译（免安装环境）

本人推荐使用 [LoongTex](https://app.loongtex.com/) 或 Overleaf 进行在线编写：

1. 将本项目的所有文件（`template.tex` 和 `images` 文件夹）上传至在线编辑器的项目中。
2. 将编译器设置为 **XeLaTeX**（重要！处理中文字体必须使用此编译器）。
3. 直接点击编译即可生成 PDF。

### 本地编译（需安装 TeX Live / MacTeX）

如果你习惯使用本地 VS Code 等工具：

```bash
# 在终端中使用 xelatex 编译
xelatex template.tex

```

---

## ⚠️ 自定义与注意事项

* **替换头像**：请将 `images/template_avatar.png` 替换为你自己的证件照。如果比例不是完美的正方形，可以通过修改 `template.tex` 中 `\includegraphics` 的 `width` 和 `height` 参数来微调。
* **替换/取消水印**：
* 如果需要背景水印（如校徽、前司 Logo），请替换 `images/template_logo.png`。
* 如果不需要水印，请在 `template.tex` 中搜索并注释/删除 `\AddToHook{shipout/foreground}{...}` 这一段代码。


* **主题色修改**：模板默认使用科技蓝。如需修改，请在代码中找到 `\definecolor{blue}{RGB}{0, 102, 204}`，更改对应的 RGB 整数值即可全局替换。
* **页面微调**：为了尽可能多地放入项目细节，本模板使用了 `1.5cm` 的极窄页边距和紧凑的列表间距（`nosep`），这使得 A4 纸能容纳极大的信息量。如需增减间距，可搜索 `\vspace{-0.5em}` 进行局部调整。

---

*✨ 如果这个模板对你有帮助，欢迎点亮 Star!*

```

### 主要改动说明：
1. **树形目录更新**：完美匹配了你现在的同级结构，并说明了 `template_logo.png` 的水印用途。
2. **预览图更新**：把原来的 `![](./Resume_template.jpg)` 改成了引用 `./demo/template.png`，并附带了跳转 `./demo/template.pdf` 的超链接。
3. **内容针对性增强**：你的新 TeX 简历写得非常硬核（各种大模型、Agent 框架等），所以我把模板的定位描述往“IT/算法工程师”方向靠拢了，这在 GitHub 上会更吸引同领域的开发者 Star。
4. **编译提示**：特别加上了需要使用 **XeLaTeX** 编译的提示，这对包含 `ctexart` 中文包的 LaTeX 简历来说是关键防坑点。

```

---

本 README 文件由 Gemini 3.1 Pro 生成。

---