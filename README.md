# Pelican Cycle Lab

一个纯静态的 SVG 2D 动画实验仓库：鹈鹕骑自行车，并记录不同模型生成页面的测试版本。

仓库地址：[contione/pelican-cycle-lab](https://github.com/contione/pelican-cycle-lab)

在线访问：[GitHub Pages](https://contione.github.io/pelican-cycle-lab/)

## 页面与版本

- `index.html`：展示最新动画，并提供历史版本选择器。
- `versions/2026-09-17-gpt-6-astra.html`：首个独立 HTML SVG 动画页面，页面标记为 `gpt-6-astra`。
- `versions/2026-11-20-gpt-6.2-astra.html`：新版「灯塔夜班」独立 HTML SVG 动画页面，页面标记为 `gpt-6.2-astra`，测试时间为 `2026-11-20T00:12:04+08:00`（北京时间）。
- `versions.json`：版本元数据目录。

后续模型测试请新增独立 HTML 文件并更新 `versions.json`，保留已有版本；历史页面可通过目录链接单独访问。页面中的时间使用北京时间（UTC+8）记录真实测试时间，不用访问时间代替测试时间。

`versions.json` 中每条记录包含 `id`、`model`、`date`、`testedAt`、`path`。新增版本时，同时更新首页展示，并将页面的 `VERSION_ID` 设置为对应的 `id`；同一天重复测试同一模型时，在文件名及 ID 中加入时间，避免覆盖。模型名称为本次实验指定的标签。

页面支持暂停/继续、0.5–2 倍速度、重新开始，并遵循系统的减少动态效果设置。动画由内联 SVG 与 JavaScript 驱动，页面没有外部字体、图片或运行时依赖。

GitHub Pages 使用 `main` 分支根目录发布，推送后会自动更新。

项目无需安装依赖。要在本地预览，可在仓库根目录运行：

```powershell
rtk proxy python -m http.server 4173
```

然后打开 <http://localhost:4173/>。
