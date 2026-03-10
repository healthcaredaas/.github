<div align="center">
  <img src="https://via.placeholder.com/200x200?text=DataSphere" alt="DataSphere Logo" width="200">

  # HealthcareDaaS

  ### 医疗数据中台解决方案

  [![License](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
  [![GitHub Org](https://img.shields.io/badge/Organization-healthcaredaas-green)](https://github.com/healthcaredaas)

</div>

---

## 📖 项目简介

**DataSphere** 是一个面向医疗健康领域的下一代数据中台解决方案，提供数据集成、数据标准、主数据管理、元数据管理、数据质量、数据资产、数据安全、AI智能助手等核心能力。

我们致力于帮助医疗机构：
- 🔗 打通数据孤岛，实现数据互联互通
- 📊 建立数据标准，提升数据质量
- 🤖 AI赋能数据治理，降低技术门槛
- 🔒 数据安全合规，保护患者隐私

---

## 🏗️ 项目架构

```
┌─────────────────────────────────────────────────────────────────┐
│                        DataSphere 平台                           │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────────┐  │
│  │   Portal    │  │  微前端应用  │  │      AI Agent           │  │
│  │  (Vue 3)    │  │  (wujie)    │  │    (智能数据助手)         │  │
│  └─────────────┘  └─────────────┘  └─────────────────────────┘  │
├─────────────────────────────────────────────────────────────────┤
│                      API 网关 / OAuth2 认证                       │
├─────────────────────────────────────────────────────────────────┤
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐           │
│  │ 数据源   │ │ 数据集成  │ │ 数据标准  │ │ 主数据   │           │
│  │ 服务     │ │ 服务     │ │ 服务     │ │ 服务     │           │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘           │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐           │
│  │ 元数据   │ │ 数据质量  │ │ 数据资产  │ │ AI Agent │           │
│  │ 服务     │ │ 服务     │ │ 服务     │ │ 服务     │           │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘           │
├─────────────────────────────────────────────────────────────────┤
│                    DaaS Boot 基础开发框架                         │
└─────────────────────────────────────────────────────────────────┘
```

---

## 📦 核心项目

| 项目 | 描述 | 技术栈 |
|------|------|--------|
| [daas-boot](https://github.com/healthcaredaas/daas-boot) | 基础开发框架，提供核心组件和工具类 | Spring Boot 3.5, MyBatis-Plus |
| [daas-cloud](https://github.com/healthcaredaas/daas-cloud) | 微服务应用，包含认证和系统管理服务 | Spring Cloud 2025, Nacos, OAuth2 |
| [daas-fe](https://github.com/healthcaredaas/daas-fe) | 前端组件库，UI组件和核心功能模块 | Vue 3, TypeScript, Element Plus |
| [datasphere-next](https://github.com/healthcaredaas/datasphere-next) | 后端服务，数据治理核心业务服务 | Spring Boot 3.5, Dubbo, Flyway |
| [datasphere](https://github.com/healthcaredaas/datasphere) | 前端应用，微前端架构的数据管理平台 | Vue 3, wujie, Pinia |

---

## ✨ 核心功能

### 数据集成
- 支持 30+ 数据源类型连接
- 可视化数据管道配置
- SeaTunnel 批量同步引擎
- 实时 CDC 数据同步

### 数据标准
- 数据集标准化管理
- 数据元定义与映射
- 医疗行业标准支持（HL7/FHIR）

### 数据质量
- 40+ 内置质量规则模板
- 自动化质量检测任务
- 质量报告与问题追踪

### 主数据管理
- 组织机构管理
- 科室与人员管理
- 医疗字典统一管理

### AI 智能助手
- 自然语言生成 SQL
- 智能数据管道配置
- 质量规则智能生成
- 数据问题智能诊断

---

## 🚀 快速开始

### 环境要求

| 组件 | 版本 |
|------|------|
| JDK | 17+ |
| Node.js | 18+ |
| MySQL | 8.0+ |
| Redis | 7.0+ |
| Nacos | 3.0+ |
| pnpm | 8+ |

### 克隆项目

```bash
# 克隆所有项目
git clone https://github.com/healthcaredaas/daas-boot.git
git clone https://github.com/healthcaredaas/daas-cloud.git
git clone https://github.com/healthcaredaas/daas-fe.git
git clone https://github.com/healthcaredaas/datasphere-next.git
git clone https://github.com/healthcaredaas/datasphere.git
```

### 启动后端服务

```bash
# 编译基础框架
cd daas-boot && mvn clean install -DskipTests

# 编译并启动后端服务
cd ../datasphere-next && mvn clean install -DskipTests
mvn spring-boot:run -pl datasphere-service/datasphere-svc-datasource
```

### 启动前端应用

```bash
# 安装依赖
cd daas-fe && pnpm install && pnpm build

# 启动前端应用
cd ../datasphere && pnpm install
pnpm dev:portal
```

---

## 📚 文档

- [产品需求规格说明书](https://github.com/healthcaredaas/datasphere-next/tree/main/docs/PRD文档)
- [系统架构设计](https://github.com/healthcaredaas/datasphere-next/tree/main/docs/设计文档)
- [数据库设计](https://github.com/healthcaredaas/datasphere-next/tree/main/docs/设计文档)
- [API 文档](https://github.com/healthcaredaas/datasphere-next/blob/main/README.md)

---

## 🛡️ 技术栈

### 后端
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5-brightgreen)
![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-2025-brightgreen)
![Dubbo](https://img.shields.io/badge/Dubbo-3.3-orange)
![MyBatis-Plus](https://img.shields.io/badge/MyBatis%20Plus-3.5-blue)
![Nacos](https://img.shields.io/badge/Nacos-3.0-blue)

### 前端
![Vue](https://img.shields.io/badge/Vue-3.5-brightgreen)
![TypeScript](https://img.shields.io/badge/TypeScript-5.7-blue)
![Vite](https://img.shields.io/badge/Vite-6-green)
![Element Plus](https://img.shields.io/badge/Element%20Plus-2.9-409eff)
![Pinia](https://img.shields.io/badge/Pinia-2.3-yellow)

---

## 🤝 贡献指南

欢迎参与 DataSphere 项目开发！

1. Fork 目标仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

---

## 📄 许可证

本项目采用 [GNU General Public License v3.0](LICENSE) 开源许可证。

---

## 📧 联系我们

- **组织**: [healthcaredaas](https://github.com/healthcaredaas)
- **邮箱**: chenpan.ai@qq.com

---

<div align="center">
  <sub>Built with ❤️ by HealthcareDaaS Team</sub>
</div>