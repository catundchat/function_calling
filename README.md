# Function_calling

函数调用 | 网页搜索 | 知识库搜索

## 函数调用功能实现

`code/demo1.ipynb`文件展示了一个简单用例，`code/demo2.`

1. 用用户输入和预定义好的函数来来验证



## 示例
### Demo1
利用官网上调用 function calling API 搭建的小型demo

### Demo2
结合 LangChain 实现 function calling 功能

### Demo3
接下来的调用代码中给出了一个例子，展示了如何使用OpenAI的函数调用功能。这个例子使用了一个名为aiaj(AI爱家)的代理，它可以根据用户的输入调用不同的工具，并生成答案。其中定义了三个parameters,分别是
- Search: 使用SerpAPIWrapper的run方法，用于根据特定查询执行网络搜索
- Calculator: 使用LLMMathChain的run方法，可以执行简单的数学计算，不包括计算微积分和解一元二次方程
- FooBar-DB: 使用SQLDatabaseChain的run方法，可以从SQL数据库中获取信息

使用这些工具和OpenAI模型初始化了一个名为mrkl的代理。当mrkl.run被调用时，它会根据用户输入的内容，调用适当的工具并生成答案。

## 参考文献
1. [Function calling and other API updates](https://openai.com/blog/function-calling-and-other-api-updates)
2. [OpenAI function calling documentation](https://platform.openai.com/docs/guides/gpt/function-calling)
3. [Function Calling via ChatGPT API - First Look With LangChain](https://www.youtube.com/watch?v=0-zlUy7VUjg&t=2s)
4. [LangChain official Twitter Media](https://twitter.com/LangChainAI/media) 
