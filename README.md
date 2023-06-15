# function_calling
2023.6.13 OpenAI update function calling and here is a function calling demo

## 示例
### Demo1
利用官网上调用 function calling API 搭建的小型demo

### Demo2
结合 LangChain 实现 function calling 功能

### Demo3
接下来的调用代码中给出了一个例子，展示了如何使用OpenAI的函数调用功能。这个例子使用了一个名为mrkl的代理，它可以根据用户的输入调用不同的工具，并生成答案。其中定义了三个parameters,分别是
- Search: 使用SerpAPIWrapper的run方法，用于根据特定查询执行网络搜索。
- Calculator: 使用LLMMathChain的run方法，可以执行数学计算。
- FooBar-DB: 使用SQLDatabaseChain的run方法，可以从SQL数据库中获取信息。

使用这些工具和OpenAI模型初始化了一个名为mrkl的代理。当mrkl.run被调用时，它会根据用户输入的内容，调用适当的工具并生成答案。
