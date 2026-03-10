# OpenClawGuide
Guide from beginner to Pro

# OpenClaw README

## 项目介绍

OpenClaw（昵称“小龙虾”）是一款基于MIT开源协议分发的AI智能体执行网关，由资深全栈工程师Peter Steinberger研发，前身为Clawdbot/Moltbot，是2026年极具影响力的开源AI工具。

核心价值：深度融合大语言模型（LLM）推理能力与本地操作系统、第三方服务，打破传统对话AI“仅交互、不执行”的局限，实现从“对话式AI”到“行动式AI”的跨越，定位为“安全、可控、可落地”的本地自动化数字管理工具。

配套生态：ClawHub作为官方配套开源社区，提供技能共享、问题答疑、开发者协作、版本更新等服务，形成“工具+社区”的良性生态，助力用户快速上手、开发者共建优化。

## 核心特性

- 低门槛上手：无需编程技能，自然语言指令即可完成操作配置，适配非专业使用者与新手。

- 实操性极强：可直接操控本地设备，支持文件处理、浏览器自动化、系统命令调用、远程控制等各类实际任务。

- 安全可控：优先本地部署，所有数据及执行过程本地存储，开源可审计、支持自托管，保障隐私安全并控制使用成本。

- 多场景适配：覆盖个人、开发者、企业三大场景，内置53个官方核心技能、700+社区技能，支持自定义扩展。

- 灵活适配性：支持Windows、macOS、Linux三大操作系统，可对接云模型（ChatGPT、Claude等）与本地模型（Ollama接入），支持多设备联动与远程控制。

## 环境要求

### 硬件要求（最低配置）

- CPU：Intel i5/AMD Ryzen 5及以上（推荐Intel i7/AMD Ryzen 7）

- 内存：8GB及以上（本地部署模型建议16GB+）

- 存储：预留20GB+空闲空间（用于依赖、模型及数据存储）

- 网络：稳定网络（用于下载依赖、对接云模型；本地模型部署后可离线使用）

### 软件与依赖要求

- 运行时：Node.js v22及以上版本（核心依赖）

- 可选依赖：Docker（沙箱隔离，提升安全性）

- 模型支持：云模型（需API Key）或本地模型（Ollama接入，如Llama、Qwen）

- 辅助工具：Git（获取源码）、PowerShell（Windows专用，执行安装命令）

- 社区访问：浏览器（推荐Chrome、Edge，访问ClawHub）

## 快速部署（新手首选）

全程命令行操作，三大操作系统通用（以Windows为例），三步完成安装配置：

### 1. 安装核心依赖（Node.js）

1. 访问Node.js官网（https://nodejs.org/），下载v22及以上LTS版本

2. 安装时勾选“Add to PATH”，安装完成后以管理员身份启动PowerShell

3. 执行命令验证：`node -v`、`npm -v`，显示版本号即安装成功

### 2. 安装OpenClaw核心程序

在PowerShell中执行命令：`npm install -g openclaw`

终端显示“installed successfully”即安装完成，执行`openclaw onboard`启动配置向导。

### 3. 基础配置与验证

1. 选择“quickstart”模式，按提示确认配置

2. 对接模型（云模型输入API Key，本地模型需提前安装Ollama）

3. 勾选官方核心技能，执行`openclaw start`启动服务

4. 验证：输入指令“帮我整理桌面文件，按类型分类”，能正常执行即配置无误

## 目录结构（对应完整指南）

- 入门篇：初识OpenClaw + 环境准备 + 快速部署 + 新手避坑

- 基础篇：核心概念 + 基础操作 + 高频场景实操 + 技能管理

- 进阶篇：模型优化 + 技能编排 + 多智能体协同 + 云部署方案

- 精通篇：核心架构 + 二次开发 + 源码优化 + 配置优化

## 使用说明

- 交互方式：命令行（新手首选）、通讯软件（Telegram等）、Web UI（http://localhost:3000）

- 技能管理：查看（`openclaw list skills`）、安装（`openclaw install skill [技能名]`）、卸载（`openclaw uninstall skill [技能名]`）

- 任务管理：查看进度（`openclaw tasks`）、终止任务（`openclaw stop [任务ID]`）、查看日志（`openclaw logs [任务ID]`）

- 社区资源：访问ClawHub（https://clawhub.io）获取技能、教程、问题解决方案

## 常见问题

- 安装失败提示“找不到git”：安装Git并勾选“Add Git to PATH”，重启PowerShell

- 网关无法启动：检查Node.js版本，执行`openclaw status`查看日志，或前往ClawHub求助

- 模型对接失败：确认API Key正确（云模型）、Ollama服务启动（本地模型）

- 技能安装失败：手动执行安装命令，或通过ClawHub下载技能包导入

## 参考链接

- OpenClaw官方GitHub源码：https://github.com/openclaw/openclaw

- 原作者Peter Steinberger GitHub：https://github.com/petersteinberger

- ClawHub官方社区：https://clawhub.io

- Node.js官方网站：https://nodejs.org/

- Docker官方网站：https://www.docker.com/

- Ollama官方网站：https://ollama.com/

- 阿里云ECS部署文档：https://help.aliyun.com/document_detail/108014.html

- AWS EC2部署文档：https://docs.aws.amazon.com/zh_cn/ec2/index.html

- Llama模型官方网站：https://ai.meta.com/models/llama/

- Qwen模型官方网站：https://qwenlm.cn/

## 贡献方式

- 源码贡献：通过GitHub提交PR，遵循官方开发规范

- 技能分享：在ClawHub上传自定义技能，标注功能与适配版本

- 问题反馈：在GitHub Issues或ClawHub答疑板块提交问题与建议

## 开源协议

本项目基于MIT开源协议分发，详见LICENSE文件。
> （注：文档部分内容可能由 AI 生成）
