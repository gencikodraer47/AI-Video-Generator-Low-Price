# AI 图片生成器

一个简洁美观的在线 AI 图片生成工具，支持 GPT Image 2 和 Gemini 系列模型，提供最高 4K 分辨率的图片生成能力。

## 功能特点

- **多模型支持**：GPT Image 2（4K / CC）、Gemini 3 Pro、Gemini 3.1 Flash
- **高分辨率输出**：支持 1K / 2K / 4K 多种尺寸，横版竖版自由选择
- **批量生成**：单次可生成 1-4 张图片
- **质量可选**：low / medium / high 三档质量
- **历史记录**：自动保留最近 20 张生成记录，点击可回顾
- **一键下载**：生成后直接下载到本地
- **深色主题**：舒适的暗色界面，适合长时间使用
- **零依赖**：纯 HTML + CSS + JS，单文件即可运行

## 支持的模型与尺寸

| 模型 | 最大分辨率 | 分组要求 |
|------|-----------|---------|
| gpt-image-2-4k | 3840 × 2048 (4K) | SVIP 分组 |
| gpt-image-2-cc | 3840 × 2048 (4K) | SVIP 分组 |
| gemini-3-pro-image-preview | 1792 × 1024 | 默认分组 |
| gemini-3.1-flash-image-preview | 1792 × 1024 | 默认分组 |

## 快速使用

1. 下载或克隆本项目
2. 在浏览器中打开 `ai-image-generator.html`
3. 在高级配置中填入你的 API 密钥
4. 输入图片描述，点击「生成图片」

或者直接在 HTML 文件中修改默认的接口地址和密钥。

## 快捷键

- `Ctrl + Enter`：快速生成图片

## API 说明

本项目兼容 OpenAI Images API 格式，支持任意兼容该格式的第三方接口。

接口端点：`POST /v1/images/generations`

请求参数：
- `model`：模型名称
- `prompt`：图片描述
- `n`：生成数量（1-4）
- `size`：图片尺寸
- `quality`：图片质量（low / medium / high）
- `response_format`：响应格式（b64_json / url）
- `group`：分组令牌（SVIP 分组需传此参数）

## 许可证

MIT License
