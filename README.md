# Function_Calling

Function calling 可使我们能够利用模型的 NLU(Natural Language Understanding) 能力，有效地将人类语言转化为结构化数据或我们代码中的具体函数调用。这种能力在 AI 爱家小程序的各种场景中都很有用，从创建可以与其他 API 互动的聊天机器人，到文本后处理任务和从自然语言输入中提取结构化信息，都可以有效的提高回复质量。

函数调用 | 网页搜索 | 知识库搜索

WeChat 小程序：AI 爱家

## 函数调用功能实现

`code/demo1.ipynb`文件展示了一个简单用例

1. 首先定义了三个函数`get_apple_yield`, `get_current_data`, `get_history_date
2. 设置函数的各项参数: `name, description, parameters, required`
3. function 模块中一次可以定义多个函数，但是`gpt-3.5-turbo-16k-0613`会自主决定调用哪一个函数或者不调用函数使用模型能力回答
```
 "message": {
        "content": null,
        "function_call": {
          "arguments": "{\n\"time\": \"now\"\n}",
          "name": "get_current_time"
        }
```

`code/demo2.ipynb`文件展示了 function calling 的一般步骤

1. 使用预定义好的函数和用户输入来调用模型
2. 使用 LLM 回答来调用 API
3. 将 API 的 response 返回 LLM 并生成总结

`code/demo3.ipynb` 

接下来的调用代码中给出了一个例子，展示了如何使用OpenAI的函数调用功能。这个例子使用了一个名为aiaj(AI爱家)的代理，它可以根据用户的输入调用不同的工具，并生成答案。其中定义了三个parameters,分别是
- Search: 使用SerpAPIWrapper的run方法，用于根据特定查询执行网络搜索
- Calculator: 使用LLMMathChain的run方法，可以执行简单的数学计算，不包括计算微积分和解一元二次方程
- FooBar-DB: 使用SQLDatabaseChain的run方法，可以从SQL数据库中获取信息
使用这些工具和 OpenAI 模型初始化了一个名为 aiaj 的代理。当 aiaj.run 被调用时，它会根据用户输入的内容，调用适当的工具并生成答案。

## 参考文献

1. [Function calling and other API updates](https://openai.com/blog/function-calling-and-other-api-updates)
2. [OpenAI function calling documentation](https://platform.openai.com/docs/guides/gpt/function-calling)
3. [Function Calling via ChatGPT API - First Look With LangChain](https://www.youtube.com/watch?v=0-zlUy7VUjg&t=2s)
4. [LangChain official Twitter Media](https:twitter.com/LangChainAI/media) 


