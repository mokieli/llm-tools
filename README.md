# llm-tools

最初版本来自：[B站 纸鸢随风](https://www.bilibili.com/opus/1078272739661316119)

此仓库为第三方修改版的再次修改版

## 此仓库新增修改（2025年12月23日已提交PR，还未合并）

**修复推理模型流式响应中 `delta.reasoning_content` 的内容统计遗漏问题** 
- 通过 vLLM 部署推理模型时，启用 `--reasoning-parser` 参数后，模型推理内容与正文将分离输出，推理内容将通过 `delta.reasoning_content` 流式输出，正文内容则通过 `delta.content` 输出。
- 已修复此前 `delta.reasoning_content` 未被纳入统计的问题。

**实现用户设置的持久化保存**
- 点击“开始测试”时自动保存配置（服务器信息、推理引擎信息、接口信息、测试信息）至 localStorage
- 页面初始化时自动加载上次保存的配置
- 提升用户体验，避免重复设置

## 简介

大语言模型工具集

## 工具集列表

- **llm-performance-test**：本地大语言模型推理性能测试工具
