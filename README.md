# Pelecanus

**One Prompt. Multiple LLMs. Different 3D Worlds.**

[在线体验 · GitHub Pages](https://niaonao.github.io/pelecanus/) · [GitHub 仓库](https://github.com/niaonao/pelecanus)

## 关于项目

Pelecanus 是一个 AI 创意实验和交互式 3D 画廊。不同的大模型从同一个提示词出发，用 Three.js 创作“一只正在骑自行车的鹈鹕”。打开作品，可以比较各个场景的视觉风格、运动节奏和交互方式。

<details>
<summary>查看原始提示词</summary>

```text
使用 Three.js 创建一个精致、可交互的 3D 网页场景：一只鹈鹕正在骑自行车。

鹈鹕、自行车、环境、动画、灯光、摄像机和交互均通过程序实现。鹈鹕需要真实地骑自行车，并具有协调的腿部、脚踏、车轮和身体运动。

不要使用 SVG、2D Canvas、外部 3D 模型或预渲染动画。

最终输出一个可以直接在现代浏览器中运行的完整 HTML 文件。
```

灵感来源见 [Artificial Analysis 的鹈鹕骑自行车 SVG 挑战](https://artificialanalysis.ai/microevals/generate-an-svg-of-a-pelican-riding-a-bicycle-1777416860523)。

</details>

## 代表作品

### Claude Opus 5.5 · Pelican on a Bicycle

鹈鹕沿着秋日公路骑行。[打开交互作品](https://niaonao.github.io/pelecanus/html/Claude-Opus-5.5.html)

[![Claude Opus 5.5 作品实录，鹈鹕骑车穿过秋日景观](./img/opus5.5.gif)](https://niaonao.github.io/pelecanus/html/Claude-Opus-5.5.html)

### 八件作品的并排实录

从海岸公路到低多边形林间小路，八件作品各自诠释同一次骑行。[进入画廊](https://niaonao.github.io/pelecanus/#gallery)

![八件 AI 生成的鹈鹕骑行作品并排播放](./img/gif.gif)

## Gallery · 全部作品

| 作品来源 | 在线体验 |
| --- | --- |
| Claude Fable 5.2 | [打开作品](https://niaonao.github.io/pelecanus/html/Claude-Fable-5.2.html) |
| Claude Opus 5.5 | [打开作品](https://niaonao.github.io/pelecanus/html/Claude-Opus-5.5.html) |
| Claude Sonnet 5 | [打开作品](https://niaonao.github.io/pelecanus/html/Claude-Sonnet-5.html) |
| DeepSeek V4.1 Flash 1017 | [打开作品](https://niaonao.github.io/pelecanus/html/DeepSeek-V4.1-Flash-1017.html) |
| DeepSeek V4.1 Flash | [打开作品](https://niaonao.github.io/pelecanus/html/DeepSeek-V4.1-Flash.html) |
| GLM 5.3 Flash | [打开作品](https://niaonao.github.io/pelecanus/html/GLM-5.3-Flash.html) |
| GLM 5.3 | [打开作品](https://niaonao.github.io/pelecanus/html/GLM-5.3.html) |
| GPT-6 Astra | [打开作品](https://niaonao.github.io/pelecanus/html/GPT-6-Astra.html) |
| GPT-6.1 Sol | [打开作品](https://niaonao.github.io/pelecanus/html/GPT-6.1-Sol.html) |
| GPT-5.6 Luna | [打开作品](https://niaonao.github.io/pelecanus/html/GPT-5.6-Luna.html) |
| GPT-5.6 Sol | [打开作品](https://niaonao.github.io/pelecanus/html/GPT-5.6-Sol.html) |
| Gemini 3.1 Pro Preview | [打开作品](https://niaonao.github.io/pelecanus/html/Gemini-3.1-Pro-Preview.html) |
| Gemini 3.6 Flash | [打开作品](https://niaonao.github.io/pelecanus/html/Gemini-3.6-Flash.html) |
| Gemini 3.8 Flash | [打开作品](https://niaonao.github.io/pelecanus/html/Gemini-3.8-Flash.html) |
| Hy4 Preview | [打开作品](https://niaonao.github.io/pelecanus/html/Hy4-Preview.html) |
| Kimi K3.1 Pro | [打开作品](https://niaonao.github.io/pelecanus/html/Kimi-K3.1-Pro.html) |
| Kimi K3 | [打开作品](https://niaonao.github.io/pelecanus/html/Kimi-K3.html) |
| Muse Wonder | [打开作品](https://niaonao.github.io/pelecanus/html/Muse-Wonder.html) |
| Qwen 3.8 Max | [打开作品](https://niaonao.github.io/pelecanus/html/Qwen-3.8-Max.html) |
| Space Bunny Alpha | [打开作品](https://niaonao.github.io/pelecanus/html/Space-Bunny-Alpha.html) |
| Step 5 Preview | [打开作品](https://niaonao.github.io/pelecanus/html/Step-5-Preview.html) |

## 项目目录

```text
pelecanus/
├── .gitignore
├── index.html     # 画廊首页
├── html/          # 独立的 Three.js 作品 HTML，见上表
├── img/
│   ├── gif.gif
│   ├── opus5.5.gif
│   └── Artificial Analysis Intelligence Index (11 Nov '26).png
├── README.md
└── LICENSE
```

## 本地体验

下载或克隆仓库后，直接用现代浏览器打开项目根目录的 `index.html`，无需安装 Python 或启动本地服务器。也可以直接打开 `html/` 中任一作品的 HTML 文件。

浏览器需要支持 WebGL；部分作品通过 CDN 加载 Three.js，需要联网。拖拽旋转、缩放或调节骑行速度等操作以各作品内的提示为准。

## 最近上新

- 2026-11-11：新增 [Claude Fable 5.2](html/Claude-Fable-5.2.html)。

## 参考与演示

- 项目说明：[CSDN 博客](https://blog.csdn.net/niaonao/article/details/165008168) · [掘金文章](https://juejin.cn/post/7684937171811221513)
- 视频演示：[Bilibili](https://www.bilibili.com/video/BV11GYv6oEJG/)

<details>
<summary>AA 智能榜单快照（2026-11-11）</summary>

下图是 Artificial Analysis Intelligence Index 在 2026-11-11 的快照，仅供背景参考，不代表本仓库作品的排名。点击图片可查看[最新交互榜单](https://artificialanalysis.ai/models#intelligence)。

[![Artificial Analysis Intelligence Index（2026-11-11）](img/Artificial%20Analysis%20Intelligence%20Index%20%2811%20Nov%20%2726%29.png)](https://artificialanalysis.ai/models#intelligence)

</details>

## License

[Apache License 2.0](./LICENSE)
