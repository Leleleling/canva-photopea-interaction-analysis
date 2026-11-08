# 引用与证据来源清单（assets/references.md）

> 本文件归档本仓库引用的公开资料（`[DOC]`）与一手取证文件（`[OBS]`），便于回溯与校验。
> 采集时点：2026-11。

## A. 一手取证文件（[OBS]，Photopea 本机实跑）

路径前缀：`assets/`

| 文件 | 内容 |
| --- | --- |
| `photopea-01-home.html` | Photopea 落地页 DOM（含「Start using Photopea」入口） |
| `photopea-editor-after.html` | 编辑器加载后 DOM（topbar/panelblock/tools/canvas 等类名） |
| `photopea-topbar.json` | 顶栏菜单文本（10 个菜单，中文） |
| `photopea-menu-文件-dropdown.json` | 文件菜单下拉项：新建项目/从电脑打开/模板/安装 Photopea/Generate Video |
| `photopea-newproject.json` | 新建项目对话框：预设（打印/照片/屏幕/移动/广告）、创建按钮 |
| `photopea-editor-doc.json` | 文档态：3 个 canvas（主画布 1011×951）、19 个工具栏、12 个面板、图层/通道/路径、历史/色板、混合模式、选项栏 |
| `photopea-menu-*.json` / `photopea-menus-items.json` | 菜单展开尝试记录（部分下拉为画布内绘制，未稳定捕获） |
| `photopea-0*.png` | 主界面/编辑器/菜单/新建文档截图（部分菜单截图因字体等待超时留空，仅作归档） |

## B. 公开资料（[DOC]）

### Canva 编辑器结构
- Canva 编辑器无障碍说明（侧面板标签、顶部导航、快捷键原文）：
  `https://www.canva.com/design/play?category=tAG10WuVVlc&locale=en` （及中文站 `https://www.canva.cn/design/play?...&locale=zh-CN`）
- 第三方教程对四区布局/快捷键的一致描述（websitebuilder.com.tw 等搜索结果）。

### Canva PDF 编辑器 / PDF 编辑特性
- 在线 PDF 编辑器（Canva 中文官网）：`https://canva.cn/pdf-editor/`
- 免费导入和编辑 PDF（Canva 特性页）：`https://www.canva.cn/features/pdf-editing` 与 `https://www.canva.cn/features/pdf-editing/`
- Free Online PDF Editor（国际站）：`https://www.canva.com/pdf-editor`
- PDF Page Remover（页面操作佐证）：`https://canva.com/features/delete-pages-from-pdf`

> 关键 `[DOC]` 事实：导入即拆解 PDF 为可编辑元素；改文字/图、线条/形状/签名/批注；页面增删/旋转/重排/提取/拆分；合并 PDF；云同步/评论；导出 PDF/JPG/PNG/SVG/PPT；上限 100MB/300 页。

### Photopea（公开特性，用于补全未实抓的子项）
- Photopea 官网与帮助：`https://www.photopea.com` 、`https://www.photopea.com/learn` 、`https://www.photopea.com/tuts`
- 关键 `[DOC]` 事实：Fully Local（不上传原图、本地运行）、支持 PSD/PXD/SVG/PDF 与多种位图导入导出。

## C. 推断标注（[INF]）

凡文中标记为 `[INF]` 的结论，均基于上述 `[OBS]`/`[DOC]` 的合理推测（如 Canva 的服务端导出、Photopea 的命中测试与历史栈实现），非一手观察，阅读时请留意区分。
