# 简历项目提纲

本文件只作为结构模板。标为“待补充”的内容必须由真实测试或报告提供，不得编造。

## 基本信息

- 姓名：待填写
- 求职方向：Java 后端 / AI 应用平台后端
- 目标城市：深圳
- GitHub：`https://github.com/stoneethan`
- 教育背景：计算机相关本科

## 技能

- Java 17、集合、并发、JVM 基础。
- Spring Boot、Spring Cloud Alibaba、Nacos、Gateway、OpenFeign、Sentinel。
- MySQL、Redis、RabbitMQ、Qdrant、MinIO。
- Spring AI、RAG、Embedding、混合检索、SSE。
- JUnit 5、Testcontainers、Docker Compose、GitHub Actions。

技能只列能够解释并至少有练习证据的内容。

## 项目：AI Knowledge Platform

项目简介：

> 面向多 Workspace 的企业知识库平台，使用六个 Java 微服务完成文档异步摄取、混合检索和带引用的流式问答。

建议采用“动作 + 技术 + 结果”的 bullet：

- 使用 Spring Cloud Alibaba、Gateway、Nacos 和 OpenFeign 拆分认证、文档、检索、聊天和模型网关，实现服务发现与统一入口。
- 使用 RabbitMQ 构建异步文档摄取链路，通过事件去重、重试和死信队列处理重复消费与解析失败。
- 使用 Spring AI、Qdrant Dense + BM25 + RRF 和 Spring AI Advisor 完成多 Workspace RAG，返回可核验引用。
- 使用 SSE 实现流式回答，记录模型、Token、Prompt 版本和耗时。
- 使用 Sentinel、超时和熔断实现国内 API 到 Ollama 的聊天降级，并固定 Embedding 模型避免向量空间混用。
- 使用 Testcontainers 覆盖跨 Workspace 隔离、重复消息、检索和模型降级场景，核心链路覆盖率达到“待补充”。
- 在 2C4G 环境完成部署；50 并发下达到“待补充”的错误率和 P95 延迟。
- 基于 30 条黄金问答评估检索，Hit@5 达到“待补充”。

## 当前非开发工作经历

只写实际做过且可以解释的内容，例如：

- 业务需求梳理和跨部门协调。
- 系统运维、问题排查和流程改进。
- 实际参与过的内部自动化或开发任务。

禁止把公司内部未完成的计划、他人代码或敏感系统写为自己的开发成果。

## 面试前删除

- 没有证据的“精通”。
- 无法解释的框架名。
- 与目标岗位无关且占空间的课程列表。
- 夸张的覆盖率、并发量、用户量或性能数字。
