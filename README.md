# Pelecanus · 鹈鹕骑行 3D

同一个提示词，不同大模型，会创造出怎样的 3D 世界？

本仓库收录了 16 个由不同大模型生成的 Three.js 单文件作品。每个版本都围绕“一只鹈鹕正在骑自行车”展开，并尝试仅通过程序完成角色、自行车、环境、动画、灯光、摄像机与交互。

![鹈鹕骑行 3D 作品对比](img/pelicans-riding-comparison.png)

## 从经典测试题到 3D 挑战

“鹈鹕骑自行车”最初是一道经典的大模型 SVG 生成测试题：

```text
Generate an SVG of a pelican riding a bicycle
```

它用一句简短的提示词，同时考察模型对物体结构、空间关系、画面构图以及 SVG 代码生成的理解。随着大模型能力持续提升，完成一幅静态 SVG 已经越来越难以充分检验当下模型的综合能力，也难以拉开不同模型之间的差异。

因此，本仓库将经典题目升级为可交互的 3D 网页挑战：从静态二维图形扩展到程序化三维建模、材质与灯光、摄像机控制、实时交互，以及鹈鹕身体、自行车车轮、曲柄、脚踏和腿部之间协调一致的骑行动画。这里记录的不只是一次横向展示，也是一份会随着大模型发展持续演进的能力测试样本。

## 提示词

```text
使用 Three.js 创建一个精致、可交互的 3D 网页场景：一只鹈鹕正在骑自行车。

鹈鹕、自行车、环境、动画、灯光、摄像机和交互均通过程序实现。鹈鹕需要真实地骑自行车，并具有协调的腿部、脚踏、车轮和身体运动。

不要使用 SVG、2D Canvas、外部 3D 模型或预渲染动画。

最终输出一个可以直接在现代浏览器中运行的完整 HTML 文件。
```

## 作品一览

| 模型 | 查看作品 |
| --- | --- |
| Claude Sonnet 5 | [打开 HTML](html/Claude-Sonnet-5.html) |
| DeepSeek V4.1 Flash | [打开 HTML](html/DeepSeek-V4.1-Flash.html) |
| Gemini 3.1 Pro Preview | [打开 HTML](html/Gemini-3.1-Pro-Preview.html) |
| Gemini 3.6 Flash | [打开 HTML](html/Gemini-3.6-Flash.html) |
| Gemini 3.8 Flash | [打开 HTML](html/Gemini-3.8-Flash.html) |
| GLM 5.3 | [打开 HTML](html/GLM-5.3.html) |
| GLM 5.3 Flash | [打开 HTML](html/GLM-5.3-Flash.html) |
| GPT-5.6 Luna | [打开 HTML](html/GPT-5.6-Luna.html) |
| GPT-5.6 Sol | [打开 HTML](html/GPT-5.6-Sol.html) |
| GPT-6 Astra | [打开 HTML](html/GPT-6-Astra.html) · [观看录屏](screenrecord/GPT-6-Astra.mp4) |
| GPT-6.1-Sol | [打开 HTML](html/GPT-6.1-Sol.html) |
| Hy4-preview | [打开 HTML](html/Hy4-Preview.html) |
| Kimi K3 | [打开 HTML](html/Kimi-K3.html) |
| Qwen 3.8 Max | [打开 HTML](html/Qwen-3.8-Max.html) |
| Space-Bunny-Alpha | [打开 HTML](html/Space-Bunny-Alpha.html) |
| Step-5-Preview | [打开 HTML](html/Step-5-Preview.html) |

> 这里展示的是各模型的原始生成结果，仓库不对作品进行排名。相关说明与演示见文末链接。

## 快速体验

克隆仓库后，在项目根目录启动一个静态文件服务器：

```bash
git clone <repository-url>
cd pelecanus
python -m http.server 8000
```

然后访问：

```text
http://localhost:8000/html/GPT-6-Astra.html
```

也可以把地址末尾替换为上表中的其他 HTML 文件名。

部分作品通过 CDN 加载 Three.js，首次打开时需要保持网络连接。推荐使用最新版 Chrome、Edge、Firefox 或 Safari，并确保浏览器支持 WebGL。

## 交互方式

各版本的交互设计并不完全相同，常见操作包括：

- 鼠标拖拽旋转视角，滚轮缩放场景；
- 切换跟随、自由或电影视角；
- 暂停或继续骑行动画；
- 调节骑行速度、切换昼夜或触发车铃；
- 使用页面提示的键盘快捷键。

具体功能请以每个作品页面中的操作提示为准。

## 项目特点

- **纯程序化 3D 场景**：鹈鹕、自行车与环境均由 Three.js 几何体和材质构建；
- **骑行动画联动**：重点观察腿部、脚踏、曲柄、车轮与身体起伏之间的协调；
- **单文件交付**：每个模型的结果都保存在独立 HTML 文件中，便于查看与对比；
- **多种交互尝试**：不同版本包含各自的镜头、速度、光照、音效和场景控制设计；
- **原始结果留档**：保留模型输出，方便复现、展示和后续研究。

## 目录结构

```text
pelecanus/
├── html/          # 各模型生成的 Three.js 单文件作品
├── img/           # 项目预览与对比图片
├── screenrecord/  # 作品演示录屏
├── LICENSE
└── README.md
```

## 说明

模型名称仅用于标识生成作品的来源。本项目与相关模型厂商不存在官方隶属或背书关系；各作品效果受生成时使用的模型版本、提示词和运行环境影响。

## License

本项目采用 [Apache License 2.0](LICENSE) 许可证。

## 博客说明

- [CSDN 博客](https://blog.csdn.net/niaonao/article/details/165008168)
- [掘金文章](https://juejin.cn/post/7684937171811221513)

## Bilibili 视频

- [鹈鹕骑行 3D 演示](https://www.bilibili.com/video/BV11GYv6oEJG/)

## 鹈鹕骑行案例来源

- [Artificial Analysis：Generate an SVG of a pelican riding a bicycle](https://artificialanalysis.ai/microevals/generate-an-svg-of-a-pelican-riding-a-bicycle-1777416860523)
