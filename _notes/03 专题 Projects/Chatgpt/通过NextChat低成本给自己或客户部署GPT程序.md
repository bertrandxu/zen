---
title: 通过NextChat部署GPT程序
date created: 2024-03-17
date modified: 2024-03-17
tags:
---
## 引言

在国内，用着别人的GPT总归不爽，一是担心稳定性，二是还可能被广告打扰。Github上超人气项目NextChat提供了私有化部署GPT的最佳实践方案，帮助你低成本完成GPT的私人所有。

先看看最终搭建的网站[Demo](https://1aichat.top/) （如果看不到网站，可能需要使用魔法）

学习如何使用NextChat程序建议阅读文章：[[ChatGPT操作指南]]

## 什么是NextChat（ChatGPT-Next-Web）

**[NextChat](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web)（又名ChatGPT-Next-Web，以下简称NextChat）** 是一个面向用户的GPT类应用程序，用户可以通过这个程序与GPT进行交互。目前市面上已出现很多GPT类应用程序，除了本文重点介绍的NextChat以外，还有[OpenAI官方GPT（含Plus）](https://openai.com/)、[LobeChat](https://github.com/lobehubbot/lobe-chat)、[ChuanhuChatGPT](https://github.com/GaiZhenbiao/ChuanhuChatGPT)、[chatgpt-web-midjourney-proxy](https://github.com/Dooy/chatgpt-web-midjourney-proxy)、[ChatBox](https://github.com/Bin-Huang/chatbox)、[gpt_academic](https://github.com/sunsky89757/gpt_academic)、[ChatGPT-Web](https://github.com/sunsky89757/ChatGPT-Web)等，其余项目均可前往Github作者仓库进行进一步研究使用。该项目在Github已经斩获55.6kstar，当之无愧的GPT程序NO.1，并且据悉目前该项目已被收购，商业价值潜力巨大。

**NextChat官方介绍：**

一键免费部署你的跨平台私人 ChatGPT 应用, 支持 GPT3, GPT4 & Gemini Pro 模型。

**NextChat主要功能：**

- 在 1 分钟内使用 Vercel 免费一键部署
- 提供体积极小（~5MB）的跨平台客户端（Linux/Windows/MacOS）, [下载地址](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web/releases)
- 完整的 Markdown 支持：LaTex 公式、Mermaid 流程图、代码高亮等等
- 精心设计的 UI，响应式设计，支持深色模式，支持 PWA
- 极快的首屏加载速度（~100kb），支持流式响应
- 隐私安全，所有数据保存在用户浏览器本地
- 预制角色功能（面具），方便地创建、分享和调试你的个性化对话
- 海量的内置 prompt 列表，来自[中文提示词>>](https://github.com/PlexPt/awesome-chatgpt-prompts-zh)和[英文提示词>>](https://github.com/f/awesome-chatgpt-prompts)
- 自动压缩上下文聊天记录，在节省 Token 的同时支持超长对话
- 多国语言支持：English, 简体中文, 繁体中文, 日本語, Español, Italiano, Türkçe, Deutsch, Tiếng Việt, Русский, Čeština, 한국어, Indonesia
- 拥有自己的域名？好上加好，绑定后即可在任何地方无障碍快速访问

## 为什么选择NextChat作为GPT程序

目前有两个入口在使用该程序，分别为：

- [ChatGPT-3.5>>](https://1aichat.top/)
- [ChatGPT-4.0-Turbo>>](https://aichatpro.top/)

为什么选择它，综合NextChat主要功能介绍的那11条主要功能以及长期使用此程序的一点心得，本人认为选择NextChat理由就8个字：

- **交互丝滑**
- **界面精美**

当你用的多了，时间久了，你就知道不卡顿的程序，其丝滑的交互体验对你是多么重要，加上恰到好处的界面UI设计，可以“精致而优雅”的保持和GPT的交流热情，其体验甚至超过官方提供的网页端交互程序。目前看来，尚没有任何其他GPT程序能与之匹敌，这就是为什么使用NextChat的核心理由所在。

## 部署NextChat程序的两种方式

作者在项目ReadMe中列出了许多部署方式，有兴趣的可以选择适合自己的进行尝试，本文重点介绍最实用的两种方式，可视化本地安装（Windows为例）和可视化远程部署（Vercel部署）。两种方式分别准备条件和特点如下：

- **本地安装**：一台Windows电脑即可，0成本且无需设置；只能当前设备使用，其他人或其他设备使用需重新安装程序。**适用于不愿意折腾，仅简单自用的场景。**
- **远程部署**：一个域名，通过域名访问可多人共享，可自定义配置；部署稍复杂，有一点域名的成本（约80元/年）。**适用于多人使用或者分享给客户使用的场景。**

以上两种方案都无需自备服务器，Vercel的存在使得部署成本大大节约了。

## 方式一：本地安装

[![NextChat安装](https://www.gptacg.com/wp-content/uploads/2023/12/QQ%E6%88%AA%E5%9B%BE20231229160520.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/QQ%E6%88%AA%E5%9B%BE20231229160520.webp)

进入项目程序版本发布界面，下载对应的exe程序并安装。

![](https://pic.imgdb.cn/item/65fae07d9f345e8d0393cc08.png)

安装完成后，点开设置并修改以下两个参数：

- 替换接口地址：将原地址替换为https://api.gptacg.com
- 输入API-Key，如需人工咨询也可加微信**bertrandxu**，因市面上提供的API-Key很难分辨模型真假，稳定性也比较差，很难找到靠谱渠道。所以我们踩过坑以后自建团队搭建了专线渠道，专门用于打造高质量低价格的API-Key供应，一方面自用，另一方面共享给有需要的人。目前已支持接入10+月用量在1w刀以上的企业）
- 添加自定义模型：gpt-4-all,dalle-3

[![NextChat设置](https://www.gptacg.com/wp-content/uploads/2023/12/QQ%E6%88%AA%E5%9B%BE20231229160848.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/QQ%E6%88%AA%E5%9B%BE20231229160848.webp)

至此本地安装设置完成，可新建聊天并开始使用。

## 方法二：Vercel部署

注意：此方法在安装部署环节可能需要**借助[魔法](https://clashnode.xyz/)**，同时需准备**一个域名**。

如果觉得自己部署嫌麻烦，可以联系我们代为部署（微信号bertrandxu)。

**什么是Vercel?**

相信经常使用Github的人一定对Vercel不陌生，这里不做专业解释，你只需要知道Vercel充当了一台云服务器的作用就可以了，它可以让你在Github上的代码运行起来，从而变成一个可以访问的网站。

**什么是域名？**

如果域名还不太了解，建议去查一下，这里也不做专业解释。域名在这里的作用是让你部署完成后，**无需魔法即可访问你的GPT程序**。建议直接前往[阿里云>>](https://www.aliyun.com)注册账号并购买域名，并按照步骤完成实名认证，等待下一步使用。

**部署第一步：获取程序源码**

打开[Github网站>>](https://github.com/)并登录（如果没有账号，自行完成注册即可），搜索ChatGPT-Next-Web或直接[打开此链接>>](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web)进入作者代码仓库。找到Fork按钮并根据提示完成Fork到自己仓库的全部操作。

[![fork作者仓库](https://www.gptacg.com/wp-content/uploads/2023/12/fork%E4%BD%9C%E8%80%85%E4%BB%93%E5%BA%93.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/fork%E4%BD%9C%E8%80%85%E4%BB%93%E5%BA%93.webp)

[![完成fork](https://www.gptacg.com/wp-content/uploads/2023/12/%E5%AE%8C%E6%88%90fork.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/%E5%AE%8C%E6%88%90fork.webp)

**部署第二步：打开Vercel并新建项目。**

[Vecel官网>>](https://vercel.com/)可以直接用Github账号登录，这样也能直接关联自己的仓库，方便拉取代码。登录后会进入我的面板，点击黑色按钮Add New并选择下拉框中的Project。

[![vercel新增项目](https://www.gptacg.com/wp-content/uploads/2023/12/%E6%96%B0%E5%A2%9E%E9%A1%B9%E7%9B%AE.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/%E6%96%B0%E5%A2%9E%E9%A1%B9%E7%9B%AE.webp)

搜索ChatGPT-Next-Web仓库并导入。

[![vercel导入仓库](https://www.gptacg.com/wp-content/uploads/2023/12/vercel%E5%AF%BC%E5%85%A5%E4%BB%93%E5%BA%93.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/vercel%E5%AF%BC%E5%85%A5%E4%BB%93%E5%BA%93.webp)

添加环境变量。环境变量参数和示例可参考[**作者文档>>，**](https://github.com/sunsky89757/ChatGPT-3.5/blob/main/README_CN.md)也可参考下方列表（注意：后续如果作者更新变量，下方列表可能会失效）：

- OPENAI_API_KEY：可前往[Openai]([OpenAI Platform](https://platform.openai.com/))购买，但是有诸多限制，也可以找我（微信号：bertrandxu）购买；
- CODE：访问密码，可以使用逗号隔开多个密码；
- BASE_URL： https://api.gptacg.com；
- HIDE_USER_API_KEY：如果你不想让用户自行填入 API Key，此变量设置为 1 即可；
- DISABLE_GPT4：如果你不想让用户使用 GPT-4，此变量设置为 1 即可；
- ENABLE_BALANCE_QUERY：如果你想启用余额显示，此变量设置为 1 即可；
- CUSTOM_MODELS：用来控制模型列表，使用 + 增加一个模型，使用 – 来隐藏一个模型，使用 模型名=展示名 来自定义模型的展示名，用英文逗号隔开。示例：`+qwen-7b-chat,+glm-6b,-gpt-3.5-turbo,gpt-4-1106-preview=gpt-4-turbo` 表示增加 `qwen-7b-chat` 和 `glm-6b` 到模型列表，而从列表中删除 `gpt-3.5-turbo`，并将 `gpt-4-1106-preview` 模型名字展示为 `gpt-4-turbo`。 如果你想先禁用所有模型，再启用指定模型，可以使用 `-all,+gpt-3.5-turbo`，则表示仅启用 `gpt-3.5-turbo；此处建议写法为：**-all,+gpt-3.5-turbo,+gpt-4-1106-preview,+gpt-4-all,+dalle-3,gpt-4,gpt-4-32k**`

注意，环境变量不是必须项，可跳过执行下一步。配置环境变量是为了更加方便，例如你填写了API-Key，日常使用中则无需在设置中维护API-Key了。

[![设置环境变量](https://www.gptacg.com/wp-content/uploads/2023/12/%E8%AE%BE%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/%E8%AE%BE%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F.webp)

**部署第三步：绑定域名。**

前往阿里云将域名（顶级域名或二级域名均可，如www.example.com）A解析至IP：**76.223.126.88**。然后在Vercel中添加该域名（Vercel或自动为域名添加SSL证书，打开地址是https开头）。

[![绑定域名指引](https://www.gptacg.com/wp-content/uploads/2023/12/%E7%BB%91%E5%AE%9A%E5%9F%9F%E5%90%8D%E6%8C%87%E5%BC%95.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/%E7%BB%91%E5%AE%9A%E5%9F%9F%E5%90%8D%E6%8C%87%E5%BC%95.webp)

[![管理页面](https://www.gptacg.com/wp-content/uploads/2023/12/%E7%AE%A1%E7%90%86%E9%A1%B5%E9%9D%A2.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/%E7%AE%A1%E7%90%86%E9%A1%B5%E9%9D%A2.webp)

打开域名检查，如果可正常访问即证明部署成功。

[![打开界面](https://www.gptacg.com/wp-content/uploads/2023/12/%E6%89%93%E5%BC%80%E7%95%8C%E9%9D%A2.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/%E6%89%93%E5%BC%80%E7%95%8C%E9%9D%A2.webp)

## 常见问题

**1、我部署好之后，我的域名为什么需要魔法才可以访问？**

这是因为解析地址被墙了，更换为上文中对应的解析IP即可解决。

**2、我的程序为什么图标显示不出来？**

这是因为emoji的cdn解析地址被污染导致，遇到这种情况只能等待作者更新cdn地址或等待一段时间后再观察图标显示情况，大部分情况会被自动修复。

**3、作者后续更新了版本，我该如何更新部署好的程序？**

如果是fork作者的项目，则在Sync fork出更新即可。

[![fork更新](https://www.gptacg.com/wp-content/uploads/2023/12/fork%E6%9B%B4%E6%96%B0.webp)](https://www.gptacg.com/wp-content/uploads/2023/12/fork%E6%9B%B4%E6%96%B0.webp)

如果是clone作者的项目，则需要借助githun desktop + git命令解决。

**4、我想部署多个程序，该怎么操作？**

建议clone项目到自己仓库并部署，至于如何保持更新，请参考常见问题第3条（上一条）。

**5、如何修改模型自定义名称？**

参考文章[[ChatGPT-Next-Web修改模型显示为自定义名称]]

**6、如何修改界面文字信息？**

常见修改内容在以下几个文件：

- 修改下拉模型列表：app/constant.ts
- 修改主界面左侧信息：app/components/sidebar.tsx
- 修改欢迎语等对话内容：app/locales/cn.ts
- 修改TDK信息：app/layout.tsx
- 修改默认设置：app/store/config.ts

**7、NextChat有哪几个延伸版本？**

- 有个作者结合langchain开发了插件版，项目地址：[ChatGPT-Next-Web-LangChain>>](https://github.com/Hk-Gosuto/ChatGPT-Next-Web-LangChain)
- 有人拿去做了会员付费版本，项目地址（不推荐购买）：[AIChatWeb>>](https://github.com/Nanjiren01/AIChatWeb)
- 3.5的潘多拉版本：项目地址：[ChatGPT-AccessToken-Web>>](https://github.com/xueandyue/ChatGPT-AccessToken-Web?tab=readme-ov-file)

**8、该程序如何上传文件？**

目前该程序不支持直接上传文件，如需上传可以用我部署的[上传网站>>](https://up.gptacg.com/upload.php)，上传文件成功后获得url地址并喂给GPT进行问答，目前支持识别url文档的模型为gpt-4-all，购买的API-Key中已内置此模型，[购买地址>>](https://one.meithink.com/)。

## 总结

NextChat程序是一款基于GPT的卓越实践方案，它为用户提供了无缝的交互体验、精心设计的界面以及多端响应式布局等一系列优势。与官方程序相比，NextChat被认为更加舒适和便捷，让用户沉浸在高效的交流和互动中。部署NextChat程序可以快速获得全部功能权限，为用户的工作和学习带来极大的便利和便捷。