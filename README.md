# 晴岚纪行 · 星港探险

一款中文单机精灵养成 RPG。以晴岚星港为起点，探索浮空群岛，点亮三枚航路信标，再前往星门遗迹。

## 开始游玩

- 浏览器版：构建后打开 `dist/index.html`，可离线游玩。
- Flash 版：构建后将 `dist/Starport.swf` 放入 [Ruffle](https://ruffle.rs/) 播放。
- 两个版本使用各自播放器的本地存档。

## 开发环境

- Haxe 4.3+
- Node.js
- Playwright Chromium（用于素材/Flash 构建流程）

## 构建

在仓库根目录运行：

```bash
node tools/build.mjs
```

脚本会从 `src/`、`art/` 生成浏览器版和 SWF 版构建产物。若构建工具依赖未安装，请先按本地开发环境安装 Haxe、Node.js 与 Playwright Chromium。

## 测试

```bash
haxe -cp src -cp tests -main DuelTest --interp
```

## 项目结构

- `src/`：Haxe 游戏源码，包括探索、战斗、精灵养成、首领挑战、孵化舱和 UI。
- `art/`：场景背景、精灵立绘、矢量素材和字体资源。
- `preview/`：玩法与界面预览图、动图。
- `tests/`：战斗与养成逻辑测试。
- `tools/`：构建与美术资源处理脚本。
- `dist/`：可分发的浏览器版和 Flash 构建产物。

## 大文件说明

`dist/index.html` 和 `*.swf` 通过 Git LFS 管理。克隆仓库后请先安装 Git LFS：

```bash
git lfs install
git lfs pull
```

美术素材来源与处理记录见 [art/ART.md](art/ART.md)。

## 游戏内容

首章从晴岚星港出发，探索风芽林、潮汐湾和烬岩高地，收服并培养原创精灵，挑战九星首领，收集精灵蛋并前往星门遗迹。游戏支持键盘和鼠标操作，方向键移动，M 打开星图，Tab/Enter/Esc 用于界面操作。

---

本仓库为《晴岚纪行 · 星港探险》项目源代码与资源。
