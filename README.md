# MCJS 双端发布版 (PC & Mobile)

![Size](https://img.shields.io/badge/Size-840KB-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20PC%20%7C%20Mobile-blue)
![AI%20Generated](https://img.shields.io/badge/AI%20Generated-99%25%20Restored-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 项目简介

MCJS 是一款极度轻量、却在还原度上令人惊叹的网页版 Minecraft 项目。

本项目的核心代码基础来源于 B站 UP主“小哲”（GitHub: @X1aoZhe）的开源项目 [OpusMC](https://github.com/X1aoZhe/OpusMC)。得益于现代 AI 强大的代码生成能力，这个项目在仅约 840+ KB 的极小体积下，实现了对 Minecraft 核心玩法的 99% 极高还原度。

为了让不同设备的玩家都能获得最佳体验，本项目由 **s90691565@gmail.com** 进行分支维护，并进行了深度的双端适配。现在，本项目不再局限于单一的浏览器模式，而是正式划分为 **电脑版 (PC Edition)** 与 **手机版 (Mobile Edition)** 两个独立发布包。无需复杂的安装配置，下载解压即可直接游玩。

## 原项目与致谢

- 创意与原型来源：B站 UP主“小哲”
- 原作者 GitHub：@X1aoZhe
- 原项目仓库地址：[https://github.com/X1aoZhe/OpusMC](https://github.com/X1aoZhe/OpusMC)

在此向原作者的无私分享和 AI 生成技术带来的极简代码致敬。如果没有原版 OpusMC，就不会有现在的双端适配版本。

## 双版本说明

为了让玩家能够精准选择适合自己的版本，本仓库的 Releases 页面提供了两个独立的压缩包：

### 1. 电脑版 (PC Edition)
- **适用设备**：Windows、macOS、Linux 的桌面浏览器。
- **操作逻辑**：保留了原汁原味的 PC 端操作体验，使用键盘（WASD 移动，空格跳跃）与鼠标（左键破坏，右键放置，滑动旋转视角）进行操作。
- **界面设计**：针对大屏幕进行了 UI 优化，视野更开阔，保留了经典的十字准星和快捷栏布局。

### 2. 手机版 (Mobile Edition)
- **适用设备**：iOS、Android 手机及平板设备的移动端浏览器。
- **操作逻辑**：彻底抛弃了物理键盘的限制。引入了左侧虚拟摇杆控制移动，右侧滑动屏幕控制视角旋转，右下角配备独立的跳跃、破坏、放置方块功能按键。
- **界面设计**：重新编写了响应式 CSS 布局，完美适配各种长宽比的手机屏幕，防止 UI 元素过大遮挡视野。同时针对手机触摸屏优化了多点触控的跟手性。

## 核心特性

- 极致的轻量级：整个项目（无论是 PC 版还是手机版）发布包仅 840KB+。极小的体积意味着极快的加载速度，秒开无压力，告别漫长的 Loading 界面。
- AI 驱动的奇迹：代码几乎 100% 由 AI 生成，结构精简且高效。这是一个非常典型的 AI 辅助游戏开发案例，证明了代码体积并非决定游戏表现力的唯一标准。
- 99% 的原汁原味：无论是方块的光照渲染、物理碰撞逻辑、还是挖掘与放置的交互延迟，都完美复刻了原版 Minecraft 的经典体验。
- 零配置开箱即玩：无需安装 Node.js，无需配置任何后端环境。下载、解压、双击，三步即可进入游戏。

## 下载与游玩指南

### 获取发布包
1. 请前往本仓库顶部的 **Releases** 页面。
2. 根据您的设备类型，下载对应的压缩包：
   - 电脑玩家：下载 `MCJS-PC-vX.X.zip`
   - 手机玩家：下载 `MCJS-Mobile-vX.X.zip`
3. 将下载的压缩包解压到您的设备本地。

### 运行游戏
- 电脑端：解压后，找到文件夹内的 `index.html`，直接双击即可使用 Chrome、Edge 或 Safari 等现代浏览器打开游玩。
- 手机端：将整个解压后的文件夹传输至手机存储中。使用支持本地文件运行的手机浏览器（如 Via、Alook、Kiwi 或系统自带浏览器）找到并打开 `index.html` 即可。
- 进阶提示：如果您有个人服务器，只需将解压后的文件全部上传至静态托管平台（如 GitHub Pages、Vercel 等），即可通过分享链接让其他人直接访问。

## 操作说明

### 电脑版 (PC)
- 移动：键盘 W、A、S、D 键
- 跳跃：空格键 (Space)
- 视角：鼠标移动
- 破坏方块：鼠标左键点击
- 放置方块：鼠标右键点击

### 手机版 (Mobile)
- 移动：屏幕左下角虚拟摇杆
- 跳跃：屏幕右下角跳跃图标
- 视角：在屏幕右侧空白区域滑动
- 破坏方块：对准目标方块，点击右下角挖掘图标
- 放置方块：点击右下角放置图标

## 技术栈与适配细节

- 前端核心：HTML5 + JavaScript (基于 Canvas 2D 或 WebGL 渲染)
- UI/UX 适配：CSS3 响应式布局，Media Queries 适配不同分辨率
- 输入事件处理：PC 端使用 KeyboardEvent 与 MouseEvent；Mobile 端全面重写为 TouchEvent 和 PointerEvent，并实现了虚拟摇杆的向量计算与滑动视角的防误触逻辑。
- 代码来源：基于 OpusMC (by @X1aoZhe) 重构

## 开发者信息

- 双端适配与维护：s90691565@gmail.com
- 如果您在游玩过程中遇到 Bug，或者有更好的移动端优化建议，欢迎通过邮箱联系我，或者在仓库中提交 Issues。

## 免责声明

1. 本项目仅供学习、交流和技术研究使用，严禁用于任何商业用途。
2. 本项目为开源爱好者基于 AI 生成代码的非官方修改版，与 Mojang Studios 及 Microsoft 没有任何关联。
3. 游戏内涉及的任何 Minecraft 相关美术资源（如材质、音效、UI 图标），版权均归原作者 Mojang 所有。如有侵权，请立即联系开发者删除。

---
如果你喜欢这个项目，请给个 Star 支持一下双端适配的工作！
