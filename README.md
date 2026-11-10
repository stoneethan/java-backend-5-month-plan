# 深圳 Java 后端求职：微服务 + RAG 技术作品计划

这是一个为期 22 周、每周约 13 小时的在职学习与求职执行仓库。

目标是用一个可部署、可测试、可解释的微服务 RAG 项目，证明 Java 后端工程能力，并在第 16 周开始深圳外部岗位试投。拿到书面 offer 后再搬迁，不考虑内部转岗。

## 当前状态

- 计划状态：准备启动
- 周进度：0 / 22
- 核心项目：`ai-knowledge-platform`
- 目标城市：深圳
- 开始试投：W16
- 扩大投递：W19

## 目标岗位

优先投递以下方向：

1. AI 应用平台、企业知识库、RAG 平台 Java 后端。
2. B 端 SaaS、业务中台和成长型自研团队。
3. 普通 Java 后端岗位。
4. 外包、驻场和乙方开发岗位作为首份工作的兜底。

## 技术主线

- Java 17、Spring Boot 3.5.x
- Spring Cloud 2025.0.x、Spring Cloud Alibaba 2025.0.0.0
- Spring AI 1.1.x
- MySQL 8、Redis 7、RabbitMQ、Qdrant、MinIO
- Docker Compose、GitHub Actions、2C4G 公网环境

六个核心服务：

| 服务 | 职责 |
| --- | --- |
| `api-gateway` | 路由、JWT 校验、Workspace 上下文、限流、SSE 透传 |
| `auth-service` | 用户、Workspace、RBAC、登录和刷新令牌 |
| `document-service` | 文档上传、对象存储、摄取任务和状态 |
| `retrieval-service` | 解析、分块、向量化、混合检索和引用 |
| `chat-service` | RAG 编排、会话记忆、流式回答和历史 |
| `model-gateway` | 国内 API/Ollama 路由、超时、熔断和 Token 统计 |

## 每周执行节奏

- 周一、三、五：各 90 分钟，优先编码。
- 周二、四：各 60–90 分钟，SQL、算法或源码阅读。
- 周六：4–4.5 小时，完成跨模块集成。
- 周日：2–2.5 小时，周测、复盘、文档和 Git 整理。
- 每周算法约 2.5 小时，目标累计 100 道新题和 60 道二刷。

任何没有运行、测试、提交或复盘的“看课时间”都不计为完成。

## 仓库导航

- [总计划](docs/5-month-plan.md)
- [22 周任务](docs/weekly-plan.md)
- [执行机制](docs/execution-rules.md)
- [项目架构与接口](docs/project/architecture.md)
- [阶段验收清单](docs/project/acceptance-checklist.md)
- [深圳求职执行](docs/job-search/README.md)
- [岗位跟进表](docs/job-search/tracker.csv)
- [简历提纲](docs/job-search/resume-outline.md)
- [学习资源](docs/resources.md)
- [每周复盘模板](templates/weekly-review.md)
- [每日日志模板](templates/daily-log.md)
- [阶段复盘模板](templates/stage-review.md)
- [面试记录模板](templates/interview-log.md)
- [进度看板](progress.md)

## 四周里程碑

| 时间 | 必须达到的状态 |
| --- | --- |
| W4 | Java、SQL、Spring Boot、测试和 Docker 基础可落地 |
| W8 | 六服务骨架和文档异步摄取链路跑通 |
| W12 | RAG 主链路、租户隔离、流式回答和引用可用 |
| W15 | 项目在 2C4G 公网环境可访问 |
| W18 | 项目、文档、评测、演示视频和简历完整 |
| W22 | 完成三轮模拟面试并持续投递 |

## 执行边界

- 第一优先是 Java 后端岗位，不转纯算法或纯 Python 岗位。
- 不使用现公司的源码、数据、账号、密钥或敏感业务信息。
- 不把个人项目包装成公司项目，不虚构开发工龄。
- 2C4G 公网环境不运行 Ollama、Prometheus 和 Grafana；Ollama 只用于本地开发与降级演示。
- 公网模型 Key 只通过环境变量或 GitHub Secrets 注入。

## 开始方式

从 [W1 任务](docs/weekly-plan.md#w1) 开始，先完成闭卷诊断，再决定每个基础主题的实际学习时长。当天结束前填写 [每日日志](templates/daily-log.md)，周日填写 [每周复盘](templates/weekly-review.md)。
