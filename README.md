# OpenAI API 代理 

> 目前在国内访问 OpenAI API 还是有难度的，所以用 Node.js 写了个代理小程序。好用就帮忙 Star 一下🙌

## API KEY

本文假设我们已经注册了 OpenAI 账号，如果还没有创建 API 密钥，可以如下图进行操作。

![ai-api-key.png](https://51fe.site/uploads/2301/ai-api-key.png)

> 记得本地调试时将 `${process.env.API_KEY}` 替换成你的 KEY。

## 免费部署

1. 登录 [Codesandbox](https://codesandbox.io/) 账号

没有 Codesandbox 账号的话最好关联自己的 Github 注册一个账号，以后我们就可以在这两个平台之间同步自己的项目了，非常方便。

2. 新建工程

单击 “Create”，选择一个 Node.js 模板，新建 Node.js 工程。

3. 添加依赖

在 `package.json` 中添加以下依赖：

```json
"dependencies": {
  "express": "^4.18.2",
  "http-proxy-middleware": "^2.0.6"
},
```

4. 替换代码

将 `index.js` 中的代码替换为完整的代理代码。可以从我的 [repo](https://github.com/51fe/openai-proxy/blob/master/index.js) 获取。

> 如果觉得前面几步操作麻烦，可以直接 Fork 一下我的[示例项目](https://codesandbox.io/p/sandbox/openai-proxy-ge68te)，然后继续。

5. 配置 API 密钥

左上角菜单 > “Project Settings” > “Env Variables”，填入先前生成的 API 密钥，如下图所示：

![env.png](https://51fe.site/uploads/2304/env.png)

6. 重启服务

左上角菜单 > “Restart Sandbox” 重启服务，若能在右侧看到以下预览页面说明部署没大问题。预览页面地址栏显示的就是最终生成的代理服务地址。如本项目的 https://ge68te-3000.csb.app。

![index.png](https://51fe.site/uploads/2304/index.png)

> 如果不打算分享服务，可以将 Sandbox 项目移动到草稿中私有化，可以提高服务的安全性。
