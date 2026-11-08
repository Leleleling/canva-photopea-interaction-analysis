# Photopea 取证章节

> Photopea（photopea.com）是一款**免费的在线图片/PSD 编辑器**，被称为「浏览器里的 Photoshop」。本系列为**浏览器实跑一手取证**（见 `README.md` 取证方法）。

## 本机观察基础事实（[OBS]）

| 项 | 观察结果 | 证据 |
| --- | --- | --- |
| 入口 | 落地页含「Start using Photopea」按钮，点击后加载编辑器（非独立 URL） | `photopea-01-home.html` / `photopea-editor-after.html` |
| 渲染形态 | 图像绘制在 `<canvas>` 上；UI chrome（菜单/工具栏/面板）为 DOM | `photopea-editor-doc.json`（3 个 canvas，主画布 1011×951） |
| 顶栏菜单（中文） | 文件 / 编辑 / 图像 / 图层 / 选择 / 滤镜 / 视图 / 窗口 / 更多 / 账户（共 10 项） | `photopea-topbar.json` |
| 文件菜单下拉 | 新建项目 / 从电脑打开 / 模板 / 安装 Photopea / Generate Video | `photopea-menu-文件-dropdown.json` |
| 新建项目对话框 | 预设分类：打印 / 照片 / 屏幕 / 移动 / 广告；含 2ᴺ、⇆ 等比等；按钮「创建」 | `photopea-newproject.json` |
| 左侧工具栏 | 19 个工具（含快捷键，见 `ui-structure.md`） | `photopea-editor-doc.json` |
| 右侧面板 | 图层/通道/路径、历史记录、色板；混合模式（正常/溶解/变暗/正片叠底…） | `photopea-editor-doc.json` |
| 选项栏 | 随工具变化：自动选择 / 文件夹图层 / 显示变换控件 / 距离… | 观察（面板 DOM） |

## 章节文件

- `ui-structure.md` —— 面板布局、工具栏、操作流（含工具清单与快捷键）
- `state-dataflow.md` —— 文档模型、选中态、历史栈、数据流
- `events.md` —— 指针/键盘交互、命中测试、拖拽/缩放/对齐
- `canvas-rendering.md` —— 图层、坐标系、渲染与导出/序列化

## 关键架构判断（[INF] + [OBS]）

Photopea 整体是 **「Photoshop 范式的 1:1 复刻」**：所有核心概念（图层、蒙版、通道、路径、历史、混合模式、钢笔工具、调整图层）与桌面 Photoshop 对齐；不同的是它把整套引擎跑在浏览器里，并以 `<canvas>` 作为唯一图像表面，UI 控件用 DOM 包裹在画布四周。这使它既能做到与 PSD 高度兼容，又天然跨平台、零安装。
