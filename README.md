# Grok API 代理

使用 Deno 免费代理 xAI Grok，国内直连，不限地区/网络环境，打开即用。

免费使用 Grok 强大的大语言模型，支持长上下文对话。

兼容的 OpenAI 格式，可对接 AI 编程，接入ChatBox、Cherry Studio、Cursor、Cline 等 AI 客户端。

## Deno 部署
视频教程：[Deno部署视频教程](https://b23.tv/gR7GjP8)

1. 免费创建一个 Grok API Key [https://api.x.ai](https://api.x.ai)
1. 点击 [Fork](https://github.com/Lihu-PR/Grok-zz/fork) 本项目
2. 登录/注册 Deno https://dash.deno.com/
3. 点击创建项目 https://dash.deno.com/new_project
4. 选择此项目，填写项目名字（分配域名）
5. 部署 Entrypoint 填写 `src/deno_index.ts` 其他字段留空 
6. 点击 **Deploy Project**
7. 部署成功后获得域名，可以作为Chat API的代理使用。

## 实现原理

项目通过建立反向代理服务，将请求转发至 xAI Grok API 实现。主要原理如下：

1. **请求拦截与转发**：使用 Deno 创建高效的代理服务器，拦截客户端的请求并转发到 Grok API。
2. **API格式转换**：将 OpenAI 格式的请求自动转换为 Grok API 兼容格式，确保无缝对接。
3. **WebSocket 支持**：实现了 WebSocket 协议转发，支持流式响应，保证实时交互体验。
4. **错误处理机制**：优化的错误处理流程，确保请求失败时能够返回清晰的错误信息。

## 项目优点

1. **全球无障碍访问**：突破地域限制，在任何网络环境下都能稳定访问 Grok API。
2. **OpenAI API 兼容**：完全兼容 OpenAI 格式的 API 调用，可以无缝替换或集成到现有基于 OpenAI 的应用中。
3. **零配置部署**：通过 Deno Deploy 一键部署，无需复杂的服务器配置和维护。
4. **免费使用**：基于 Deno 的免费托管服务，无需支付额外的服务器费用。
5. **高性能**：采用轻量级设计，响应速度快，资源占用少。
6. **安全性**：请求直接转发，不存储用户敏感信息，保护用户隐私。

## 鸣谢（该项目在trueai-org的gemini项目基础上修改，支持了流式输出和Grok的API代理）

- https://github.com/tech-shrimp/gemini-playground
- https://github.com/PublicAffairs/openai-gemini
- https://github.com/trueai-org/gemini