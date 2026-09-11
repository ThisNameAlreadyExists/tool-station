# 🛠️ Tool Station

**A privacy-first suite of browser-based utilities — all processing happens locally, your files never leave your device.**

[![Live Site](https://img.shields.io/badge/Live%20Site-tools.sanzhigouzi.com-185FA5?style=for-the-badge&logo=googlechrome&logoColor=white)](https://tools.sanzhigouzi.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-ff69b4.svg?style=for-the-badge)](https://github.com/ThisNameAlreadyExists/tool-station/issues)

> 🌐 Live demo: <https://tools.sanzhigouzi.com/>
>
> 🌍 Bilingual interface (English / 简体中文) — auto-detected from browser language.

---

## 📦 What's Inside

Four independent static sites, each in its own folder:

| Path | Tool | What it does |
|------|------|--------------|
| `/` | **Portal** | A landing hub linking to all tools below. |
| `/calculator/` | **Calculator** | Loan repayment calculator with full amortization schedule (equal-payment & equal-principal). |
| `/convert-master/` | **ConvertMaster** | One-stop local file converter — images, PDFs, documents, data formats, OCR. |
| `/generator/` | **Generator** | QR code, password, color palette, UUID generators — all client-side. |

✨ Every tool runs **100% in your browser** — no server uploads, no tracking, no logins.

---

## ✨ ConvertMaster Highlights

The flagship tool — a single-file HTML app powered by CDN-loaded libraries:

- **Images**: JPG / PNG / WEBP interconversion, multi-tier compression, visual diff, multi-image → PDF, OCR text recognition, searchable PDF
- **PDF**: PDF → images (per page), PDF → text extraction, scanned PDF OCR, multi-PDF merge
- **Documents**: DOCX → HTML/TXT, TXT → PDF
- **Data**: CSV ↔ JSON, JSON prettify / minify
- **Text**: Markdown → HTML
- **Workflow editor**: drag-and-drop multi-step pipeline (compress → convert → OCR → … one click)
- **Metadata auto-strip**: EXIF / PDF metadata / Office properties
- **Bilingual i18n**, drag & drop + click + Ctrl/Cmd+V paste, OCR stats dashboard, structured error messages

## 🧮 Calculator Highlights

- Equal-payment (等额本息) and equal-principal (等额本金) loan schedules
- Full monthly breakdown: principal, interest, balance
- Export to CSV / print-friendly
- Real-time recalculation on input change

---

## 🚀 Quick Start

### Option A: Open the live site
Visit <https://tools.sanzhigouzi.com/> — no install, no setup.

### Option B: Run locally
Some features (OCR Web Workers, etc.) require an `http://` origin — opening the HTML directly via `file://` will not work.

```bash
git clone https://github.com/ThisNameAlreadyExists/tool-station.git
cd tool-station
python3 -m http.server 8765
# Then open http://127.0.0.1:8765/
```

### Option C: Deploy your own
Drop any folder onto any static host:
- Cloudflare Pages · Vercel · Netlify · GitHub Pages
- Tencent Cloud COS · Aliyun OSS · Backblaze B2
- Or `scp -r tool-station/ your-server:/var/www/your-site/public/`

---

## 🧰 Tech Stack

- **Pure HTML + CSS + JavaScript** — zero build step, single-file apps
- CDN-loaded libraries (loaded on demand):
  - `pdf-lib` — PDF manipulation
  - `PDF.js` — PDF rendering
  - `mammoth.js` — DOCX parsing
  - `Tesseract.js` — in-browser OCR
- **No frameworks, no bundlers, no dependencies to install**

---

## 🤝 Contributing & Feedback

Found a bug? Have a feature request? Please [open an issue](https://github.com/ThisNameAlreadyExists/tool-station/issues) — that's the fastest way to reach me.

Pull requests welcome. For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

[MIT](./LICENSE) © Frank Liang

---

## 中文说明

**转换大师 + 计算器 + 导航页** — 一组纯浏览器本地运行的工具站，所有处理在本地完成，文件永不上传服务器。

### 包含三个站点

| 路径 | 工具 | 功能 |
|------|------|------|
| `/` | 导航页 | 三个工具的入口聚合页 |
| `/calculator/` | 计算器 | 贷款还款明细计算（等额本息 + 等额本金，可导出 CSV） |
| `/convert-master/` | 转换大师 | 一站式本地文件转换：图片 / PDF / 文档 / 数据 / OCR / 工作流编排 |

### 转换大师主要功能

- 图片：JPG/PNG/WEBP 互转、多档压缩、多格式对比、多图合并 PDF、OCR 文字识别、可搜索 PDF
- PDF：PDF → 图片（每页）、PDF → 文本提取、扫描型 PDF OCR、多 PDF 合并
- 文档：DOCX → HTML/TXT、TXT → PDF
- 数据：CSV ↔ JSON 互转、JSON 格式化/压缩
- 文本：Markdown → HTML
- 工作流：拖拽编排多步骤串接处理（压缩 → 转格式 → OCR → … 一键执行）
- 元数据自动清除（EXIF / PDF 元数据 / Office 文档属性）
- 中英文双语 i18n，拖拽 + 点击 + Ctrl/Cmd+V 粘贴上传
- OCR 统计仪表盘（行数 / 字符数 / 置信度）

### 本地运行

OCR 等功能需通过 `http://` 协议访问（Web Worker 跨源限制），不能用 `file://` 双击打开：

```bash
python3 -m http.server 8765
# 然后访问 http://127.0.0.1:8765/
```

### 部署

单文件直传任意静态托管即可上线。

### 技术栈

- 纯 HTML + CSS + JavaScript（单文件，无构建）
- CDN 按需加载：pdf-lib、PDF.js、mammoth.js、Tesseract.js
- 浏览器本地处理，文件不上传服务器

### 反馈

请通过 [GitHub Issues](https://github.com/ThisNameAlreadyExists/tool-station/issues) 提交问题或功能建议。

### 许可

[MIT](./LICENSE) © Frank Liang
