# A11in AI 创意画布

基于 moxt.ai 制作的多模态 AI 创作画布，通过节点连接组织文本、图片、音频和视频工作流。

## 功能

- 无限画布、节点编排、缩放与小地图
- 文本、图片、音频和视频生成节点
- 项目、预设与素材管理
- 支持 moxt.ai 环境下的团队资产、广场和回收站能力

## 本地预览

使用任意静态服务器托管当前目录，例如：

```powershell
python -m http.server 8080
```

然后访问 `http://localhost:8080/main.html`。未配置第三方服务时，画布和本地编辑功能仍可使用，AI 生成功能会显示缺少配置的提示。

## 私有配置

仓库不包含任何真实密钥、账号、专用模型 Endpoint 或 webhook。若需启用生成能力：

1. 将 `config.example.js` 复制为 `config.local.js`。
2. 填写自己的服务配置。
3. 在本地预览时将 `main.html` 中的 `config.js` 改为 `config.local.js`；部署时建议由私有部署流程提供配置。

不要提交 `config.local.js`。前端应用中的密钥仍会暴露给浏览器用户，生产环境应通过自己的后端代理调用第三方 API。

## 安全说明

公开版本已经移除原开发环境中的 API Key、Token、企业账号、管理员白名单、专用模型 Endpoint、插件地址和 webhook。
