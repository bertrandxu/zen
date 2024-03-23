---
title: ChatGPT-Next-Web修改模型显示为自定义名称
date created: 2024-03-20
date modified: 2024-03-20
tags:
---
## 问题描述

如下图所示，我们有时候很难记住模型那一长串字符，是否可以通过更加直观的文字呈现方式实现？

[![模型代号](https://www.giftedpm.com/wp-content/uploads/2023/12/222-1.png)](https://www.giftedpm.com/wp-content/uploads/2023/12/222-1.png)

答案是肯定的，本文会教你如何实现自定义文字显示模型，从而代替用模型代号显示的方式，让你在选择模型的时候更加方便。

[![模型名称自定义](https://www.giftedpm.com/wp-content/uploads/2023/12/111.png)](https://www.giftedpm.com/wp-content/uploads/2023/12/111.png)

## 操作步骤

分别修改如下文件：

/app/constan.ts文件，新增“description”字段。

```javascript
export const DEFAULT_MODELS = [
  {
    name: "gpt-4",
    available: true,
  },

<!--找到从第99行开始的代码，改为如下-->

export const DEFAULT_MODELS = [
  {
    name: "gpt-4",
    description: "最强模型",
    available: true,
  },
```

/app/client/platforms/openai.ts文件，新增返回值。

```javascript
return chatModels.map((m) => ({
      name: m.id,
      available: true,
    }));

<!--找到第323行开始的代码，改为如下-->

return chatModels.map((m) => ({
      name: m.id,
      description: "",
      available: true,
    }));
```

/app/client/api.ts文件，修改LLMModel模型参数。

```javascript
export interface LLMModel {
  name: string;
  available: boolean;
}

<!-- 找到第41行开始的代码，改为如下-->

export interface LLMModel {
  name: string;
  description: string;
  available: boolean;
}
```

改完以上三个文件后，即可部署，如需添加模型，只需要在/app/constan.ts文件添加即可，其中description的值即为模型对外显示的自定义内容。