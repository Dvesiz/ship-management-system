# 🚢 船舶管理系统

[English](./README.md) | 中文文档

> 一个基于 Vue 3 + Spring Boot 3 构建的现代化船舶管理平台。从船舶档案到航次调度，一站式管理您的船队。

---

<div align="center">

![Vue](https://img.shields.io/badge/Vue-3.5.24-4FC08D?logo=vue.js)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.0-6DB33F?logo=spring)
![Element Plus](https://img.shields.io/badge/Element%20Plus-2.13.0-409EFF)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql)
![Redis](https://img.shields.io/badge/Redis-Latest-DC382D?logo=redis)
![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=java)
![License](https://img.shields.io/badge/License-MIT-green)
![GitHub stars](https://img.shields.io/github/stars/Dvesiz/Ship-Management-System?style=social)
![GitHub forks](https://img.shields.io/github/forks/Dvesiz/Ship-Management-System?style=social)
![GitHub last commit](https://img.shields.io/github/last-commit/Dvesiz/Ship-Management-System)
![GitHub repo size](https://img.shields.io/github/repo-size/Dvesiz/Ship-Management-System)
![GitHub issues](https://img.shields.io/github/issues/Dvesiz/Ship-Management-System)

<img width="1919" height="902" alt="image" src="https://github.com/user-attachments/assets/37e66d3e-4755-46b3-bc86-f55be8065cd0" />
<img width="1919" height="918" alt="7b925b9d7a1a1a2d17b4201fa836fbe6" src="https://github.com/user-attachments/assets/fba76e08-67fc-4ece-88a8-056cfc943c60" />
<img width="1919" height="905" alt="aa7ea37e9c39637fee0148c83c852b47" src="https://github.com/user-attachments/assets/6d6d4a86-0160-4574-920e-d27119ecae0b" />
<img width="1919" height="912" alt="87356a5763ad81eed959e4fe28b06938" src="https://github.com/user-attachments/assets/bc371849-e073-4843-b206-16f0c30f9c83" />


</div>

---

## 📋 目录

- [项目简介](#项目简介)
- [核心特性](#核心特性)
- [技术栈](#技术栈)
- [快速开始](#快速开始)
- [项目结构](#项目结构)
- [API文档](#api文档)
- [最近更新](#最近更新)

---

## 项目简介

船舶管理系统是一个基于 **Vue 3 + Spring Boot 3** 的现代化全栈 Web 应用，采用前后端分离架构。系统为船舶管理提供完整的数字化解决方案，涵盖船舶、船员、航次、维修保养、燃油记录、证书管理等核心业务流程。

### 🎯 设计目标

- **易用性** - 直观的用户界面，降低学习成本
- **完整性** - 覆盖船舶管理全业务流程
- **安全性** - 多层安全防护，保障数据安全
- **扩展性** - 模块化设计，易于功能扩展

---

### ✨ 项目亮点

> 🚢 **8 大业务模块** — 船舶、船员、航次、维护、燃油、证书、消息、日志全覆盖
> 🔐 **企业级安全** — JWT + Redis + RBAC + Cloudflare Turnstile 多重防护
> 📊 **数据可视化** — ECharts 统计图表，支持 Excel/PDF 一键导出
> 🏗️ **现代化架构** — Vue 3 Composition API + Spring Boot 3 + MyBatis-Plus

---

## 核心特性

### 🔧 业务功能模块

#### 1. 船舶管理
- ✅ 船舶信息增删改查
- ✅ 船舶分类管理（散货船、集装箱船等）
- ✅ 船舶状态跟踪（在役/维修中/停运/航行中）
- ✅ 封面图片上传（支持阿里云OSS/AWS S3）
- ✅ **批量删除** - 支持批量删除船舶记录

#### 2. 船员管理
- ✅ 船员档案管理
- ✅ 船员与船舶关联分配
- ✅ 职位管理（船长、大副、轮机长等）
- ✅ **批量删除** - 支持批量删除船员记录

#### 3. 航次管理
- ✅ 航次计划与执行跟踪
- ✅ 起止港口记录
- ✅ 航次状态管理（计划中/执行中/已完成）
- ✅ 时间管理
- ✅ **批量删除** - 支持批量删除航次记录

#### 4. 维修保养
- ✅ 维修记录管理
- ✅ 维修类型分类
- ✅ 费用记录与统计
- ✅ **批量删除** - 支持批量删除维修记录

#### 5. 燃油管理
- ✅ 燃油消耗记录
- ✅ 燃油类型管理（重油HFO、轻油MDO等）
- ✅ 成本分析与统计
- ✅ 供应商管理
- ✅ **批量删除** - 支持批量删除燃油记录

#### 6. 证书管理
- ✅ 船舶证书信息管理
- ✅ 证书到期自动提醒
- ✅ 证书状态自动更新
- ✅ **批量删除** - 支持批量删除证书记录

#### 7. 消息中心
- ✅ 实时消息推送（30秒轮询）
- ✅ 多类型消息（系统/维护/航次/证书）
- ✅ 消息回复功能
- ✅ 未读消息计数

#### 8. 操作日志
- ✅ AOP自动记录所有操作
- ✅ 完整的审计追踪
- ✅ 管理员查看权限

### 🔐 安全与认证

#### 认证机制
- ✅ **JWT Token 认证** - 基于 Redis 的会话存储
- ✅ **JWT 密钥配置化** - 支持生产环境动态配置
- ✅ **角色权限控制** - ADMIN/USER 双角色权限体系
- ✅ **邮箱验证码** - 注册和密码重置验证
- ✅ **人机验证** - Cloudflare Turnstile 防护

#### 安全改进 ✅
- ✅ **事务管理** - 关键业务操作添加 @Transactional 注解
- ✅ **全局异常处理** - 统一错误响应，避免敏感信息泄露
- ✅ **文件上传防护** - 添加空指针校验，防止异常
- ✅ **分层架构** - Controller → Service → Mapper 三层分离

### 📊 数据管理

- ✅ **批量删除** - 所有业务模块支持批量删除
- ✅ **Excel/PDF 导出** - 一键数据导出功能
- ✅ **数据可视化** - ECharts 图表展示统计数据
- ✅ **分页查询** - 高效的大数据量浏览
- ✅ **筛选搜索** - 多条件组合查询

---

## 技术栈

### 前端技术

| 技术 | 版本 | 用途 | 特点 |
|------|------|------|------|
| **Vue** | 3.5.24 | 核心框架 | Composition API，性能优秀 |
| **Vite** | 7.2.4 | 构建工具 | 快速冷启动，HMR |
| **Element Plus** | 2.13.0 | UI 组件库 | 美观，功能丰富 |
| **Pinia** | 3.0.4 | 状态管理 | 类型安全，DevTools 支持 |
| **Vue Router** | 4.6.4 | 路由管理 | 动态路由，导航守卫 |
| **Axios** | 1.13.2 | HTTP 客户端 | 拦截器，自动处理 Token |
| **ECharts** | 6.0.0 | 数据可视化 | 丰富的图表类型 |
| **XLSX** | 0.18.5 | Excel 处理 | 前端导出 Excel |

### 后端技术

| 技术 | 版本 | 用途 | 特点 |
|------|------|------|------|
| **Spring Boot** | 3.3.0 | 核心框架 | 自动配置，生态丰富 |
| **MyBatis-Plus** | 3.5.7 | ORM 框架 | 简化 CRUD，性能优秀 |
| **MySQL** | 8.0+ | 主数据库 | 事务支持，性能稳定 |
| **Redis** | 6+ | 缓存/会话 | 高性能，数据结构丰富 |
| **JWT** | 4.4.0 | 身份认证 | 无状态，易于扩展 |
| **Lombok** | 1.18.32 | 代码简化 | 减少样板代码 |
| **Hutool** | 5.8.26 | 工具库 | 丰富的 Java 工具 |
| **Spring Mail** | - | 邮件服务 | 邮件发送集成 |

---

## 快速开始

### 环境要求

- **Node.js** 18+
- **JDK** 17+
- **MySQL** 8.0+
- **Redis** 6+
- **Maven** 3.8+

### 1. 克隆项目

```bash
git clone https://github.com/Dvesiz/Ship-Management-System.git
cd Ship-Management-System
```

### 2. 数据库配置

创建 MySQL 数据库：

```sql
CREATE DATABASE ship_management CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

编辑后端配置文件 `ship-manage-backend/src/main/resources/application.yml`：

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/ship_management?serverTimezone=Asia/Shanghai
    username: your_username
    password: your_password
  redis:
    host: localhost
    port: 6379
    
# JWT 配置
jwt:
  secret: your-secret-key-here  # 生产环境请使用强密钥
  expiration: 86400000          # 24小时（毫秒）
  
# 邮件配置（可选）
resend:
  from-email: your-email@example.com
  api-key: your-api-key
```

### 3. 启动后端

```bash
cd ship-manage-backend

# 编译
mvn clean package -DskipTests

# 运行
mvn spring-boot:run
```

后端服务地址：`http://localhost:8088`

### 4. 启动前端

```bash
cd ship-management-front

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

前端地址：`http://localhost:5173`

### 5. 访问系统

打开浏览器访问 `http://localhost:5173`

默认管理员账号：
- 用户名：admin
- 密码：admin123

---

## 项目结构

```
ship-management-system/
├── ship-manage-backend/          # Spring Boot 后端（Java）
│   ├── src/main/java/com/dhy/shipmanagebackend/
│   │   ├── controller/           # REST API 控制器（12个）
│   │   │   ├── UserController.java
│   │   │   ├── AdminUserController.java
│   │   │   ├── ShipController.java
│   │   │   ├── CrewController.java
│   │   │   ├── VoyageController.java
│   │   │   ├── FuelRecordController.java
│   │   │   ├── ShipCertificateController.java
│   │   │   ├── MaintenanceController.java
│   │   │   ├── ShipCategoryController.java
│   │   │   ├── MessageController.java
│   │   │   ├── OperationLogController.java
│   │   │   └── FileUploadController.java
│   │   ├── service/              # 业务逻辑层
│   │   │   ├── impl/             # 服务实现（10个）
│   │   │   └── *Service.java     # 服务接口（11个）
│   │   ├── mapper/               # MyBatis 映射器（10个）
│   │   ├── entity/               # 实体类（11个）
│   │   ├── dto/                  # DTO 类
│   │   ├── utils/                # 工具类
│   │   │   ├── JwtUtil.java      # JWT 工具
│   │   │   ├── BcryptUtil.java   # 加密工具
│   │   │   └── ...
│   │   ├── annotation/           # 自定义注解
│   │   ├── aspect/               # AOP 切面（操作日志）
│   │   └── exception/            # 全局异常处理
│   └── src/main/resources/
│       ├── application.yml       # 配置文件
│       └── static/               # 静态资源
│
└── ship-management-front/        # Vue 3 前端
    ├── src/
    │   ├── api/                  # API 接口封装
    │   ├── components/           # 可复用组件
    │   ├── layout/               # 布局组件
    │   ├── views/                # 页面组件
    │   ├── stores/               # Pinia 状态管理
    │   ├── router/               # 路由配置
    │   └── utils/                # 工具函数
    └── vite.config.js            # Vite 配置
```

---

## API 文档

### 批量删除接口

所有业务模块均支持批量删除功能：

| 模块 | 接口地址 | 请求方法 | 请求体示例 | 说明 |
|------|----------|----------|------------|------|
| 用户管理 | `/admin/user/batch` | DELETE | `{"ids": [1,2,3]}` | 自动过滤当前用户 |
| 船员管理 | `/crew/batch` | DELETE | `{"ids": [1,2,3]}` | |
| 船舶管理 | `/ship/batch` | DELETE | `{"ids": [1,2,3]}` | |
| 航次管理 | `/voyages/batch` | DELETE | `{"ids": [1,2,3]}` | |
| 燃油记录 | `/fuel/batch` | DELETE | `{"ids": [1,2,3]}` | |
| 证书管理 | `/certificate/batch` | DELETE | `{"ids": [1,2,3]}` | |
| 维修保养 | `/maintenance/batch` | DELETE | `{"ids": [1,2,3]}` | |
| 船舶分类 | `/ship-categories/batch` | DELETE | `{"ids": [1,2,3]}` | |

### 用户认证接口

| 接口 | 方法 | 描述 |
|------|------|------|
| `/user/register` | POST | 用户注册（需邮箱验证码） |
| `/user/login` | POST | 账号密码登录 |
| `/user/login/email` | POST | 邮箱验证码登录 |
| `/user/send-code` | POST | 发送邮箱验证码 |
| `/user/info` | GET | 获取当前用户信息 |
| `/user/avatar` | PUT | 更新头像 |

---

## 最近更新

### 2025-01-31 重要更新 ✅

1. **安全性改进**
   - ✅ 修复 JWT 密钥硬编码问题，支持 application.yml 配置
   - ✅ 改进全局异常处理，统一错误响应格式
   - ✅ 添加日志记录，避免泄露敏感信息

2. **架构优化**
   - ✅ 重构 AdminUserController，改为分层架构（使用 Service 层）
   - ✅ 添加事务管理 @Transactional，保证数据一致性

3. **健壮性增强**
   - ✅ 修复 FileUploadController 空指针风险
   - ✅ 添加参数校验

4. **功能增强**
   - ✅ 实现全模块批量删除功能（8个模块）
   - ✅ 创建统一 DTO（BatchDeleteRequest）

---

## 配置说明

### JWT 安全配置

```yaml
jwt:
  secret: your-secret-key-here-min-32-characters-long
  expiration: 86400000
```

⚠️ **重要**：生产环境请使用复杂密钥，且长度不少于32个字符

### 文件上传配置

```yaml
spring:
  servlet:
    multipart:
      max-file-size: 50MB
      max-request-size: 50MB
```

---

## 开发计划

- [x] 基础 CRUD 功能
- [x] JWT 认证与权限控制
- [x] 批量删除功能
- [ ] Swagger API 文档
- [ ] 单元测试覆盖
- [ ] Docker 容器化部署
- [ ] CI/CD 流水线

---

## 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'feat: Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

---

## 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

---

<p align="center">
  ⭐ 如果这个项目对你有帮助，请点个 Star！<br>
  📧 有问题或建议？欢迎提交 Issue 或 PR
</p>
