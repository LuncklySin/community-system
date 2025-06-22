# 🏘️community-system 智慧社区综合服务平台 - 更多在微信 ： jackSinWu --在咸鱼：不知名选手java小鑫 --B站：不知名选手java小鑫 关注可打9折

智慧社区综合服务平台是一个集 **社区服务、便民缴费、社区互动、商城购物** 于一体的数字化综合平台，致力于提升社区居民生活便利性与管理效率，满足用户日常生活各类需求。
<img width="1242" alt="c2986b3e307e33c005311b4e2d92754" src="https://github.com/user-attachments/assets/d7ff1994-8f42-4f88-a638-c1f8cf1204f3" />

![image](https://github.com/user-attachments/assets/ef44d74d-ab22-4800-bf91-a56afde3356d)

![image](https://github.com/user-attachments/assets/59a037ba-4dab-480e-a7f8-2b39b2597868)
![image](https://github.com/user-attachments/assets/ed1a227e-199b-4003-a721-f3c7b92f43f0)
![image](https://github.com/user-attachments/assets/8335d124-e3e1-4af5-bc61-6c97e8e04331)

![image](https://github.com/user-attachments/assets/57ba4cac-5eac-47a1-a3aa-8468985f4a2c)

![image](https://github.com/user-attachments/assets/56d280a6-d5ca-4d50-a772-34a7e8422f03)

![image](https://github.com/user-attachments/assets/4dd8bee0-f771-41fb-8fa2-129fa35cb426)

<img width="1280" alt="96d1323d17d87e0882210c8af47f543" src="https://github.com/user-attachments/assets/34538ee5-fd70-43ea-9eae-704ec9d7695f" />

---

## 🛠 技术栈

- **前端**：Vue.js + Vuex  
- **后端**：Spring Boot + MyBatis + Shiro + Netty  
- **数据库**：MySQL  
- **对象存储**：MinIO

---

## 🌟 主要功能模块

### 4.1 用户管理模块

- 用户注册与登录  
- 个人信息管理  
- 地址信息管理（常住地址、配送地址）  
- 消息通知管理（系统消息、提醒、社区通知）

---

### 4.2 商品管理模块

- 商品分类管理（如日用品、食品、水果、生活服务等）  
- 商品信息管理（名称、价格、库存、图片等）  
- 商品属性管理（颜色、规格、重量等）  
- 商品评价管理（用户评价、星级评分）  
- 商品库存管理（出入库、预警提醒）

---

### 4.3 订单管理模块

- 购物车管理（添加、修改、删除购物项）  
- 订单创建与支付（支持多种支付方式）  
- 订单状态跟踪（待付款、待发货、已完成、已取消等）  
- 订单评价管理（订单完成后可提交评价）  
- 售后服务管理（退换货申请、售后处理）

---

### 4.4 社区互动模块

- 社区发帖与评论（图文并茂，交流互动）  
- 点赞与收藏功能（提升用户参与感）  
- 社区通知公告（物业或管理员发布通知）  
- 用户互动管理（内容审核、举报管理等）

---

### 4.6 后台管理模块

- 用户管理（用户信息、实名认证、黑名单）  
- 商品管理（商品上下架、编辑、分类）  
- 订单管理（订单状态处理、售后审核）  
- 社区内容管理（帖子管理、评论管理、举报处理）  
- 系统配置管理（站点信息、支付配置、消息推送）  
- 权限管理（角色设置、操作权限控制）

---

### 4.7 生活缴费模块

#### 🧍 用户端功能

- **查询缴费账单**：  
  - 查看待缴费和已缴费账单  
  - 支持按时间筛选历史账单  
- **在线缴费**：  
  - 选择缴费类型（物业、水电气）  
  - 选择缴费周期，支持微信/支付宝等在线支付  
- **缴费记录查询**：  
  - 包含支付时间、金额、账单编号等信息  
- **逾期提醒功能**：  
  - 超期账单自动提醒用户（短信/站内信）

#### 👨‍💼 管理员端功能

- **费用录入**：  
  - 物业费：按小区设定固定金额，系统定期生成账单  
  - 水费、电费、天然气费：录入用量，按单价自动计算  
- **账单管理**：  
  - 批量生成账单  
  - 修改账单状态（已支付、未支付、逾期等）  
  - 逾期提醒（站内通知、短信提醒）  
- **缴费统计**：  
  - 每月缴费金额统计  
  - 统计未缴金额与逾期账单数量  
  - 按缴费类型生成可视化图表

---

## 🚀 项目部署指南

### ✅ 环境要求

| 环境组件 | 版本要求 |
|----------|----------|
| JDK      | 11 及以上 |
| Node.js  | 16 及以上 |
| MySQL    | 8 及以上 |
| MinIO    | 任意稳定版本 |

---

### ▶ 后端启动步骤

```bash
# 1. 进入后端项目目录
cd backend

# 2. 使用 Maven 构建项目
mvn clean package

# 3. 启动 Spring Boot 应用
java -jar target/community-service.jar
```

---

### ▶ 前端启动步骤

```bash
# 1. 进入前端项目目录
cd frontend

# 2. 安装依赖
npm install

# 3. 启动前端项目
npm run serve
```

---

### ▶ MinIO 配置说明

```bash
# 启动 MinIO 示例
minio server /data --console-address ":9001"
```

- 控制台地址：[http://localhost:9001](http://localhost:9001)
- 在后端配置文件 `application.yml` 中添加：

```yaml
minio:
  endpoint: http://localhost:9000
  accessKey: your-access-key
  secretKey: your-secret-key
  bucketName: community-files
```

---

## 📁 项目目录结构

```
smart-community-platform/
├── backend/        # 后端 Spring Boot 项目
│   ├── src/main/   # Java 源码
│   ├── resources/  # 配置文件
│   ├── pom.xml     # Maven 配置
├── frontend/       # 前端 Vue 项目
│   ├── src/        # 页面与组件
│   ├── public/     # 静态资源
│   ├── package.json# 前端依赖配置
├── docs/           # 项目文档
├── README.md       # 项目说明
```

---

## 🧠 项目亮点

- 🏡 集成社区商城、论坛互动、便民缴费多场景服务  
- 📦 商城模块功能完善，支持评价、库存、售后  
- 🧾 账单管理与在线支付系统打通，适应社区管理需求  
- 🔒 支持角色权限控制与内容审核机制  
- 📊 管理后台配套齐全，操作便捷

---

## 📌 注意事项

- 请根据部署环境配置数据库、对象存储、短信服务等信息  
- 建议使用 Docker 部署 MinIO、MySQL 等中间件  
- 前端可使用 Nginx 配置反向代理与 HTTPS

---

## 📬 联系与贡献

欢迎提交 Issue、Star ⭐、Fork 本项目。如有合作或需求交流可联系我：

- 📧 邮箱：example@example.com <!-- 替换为真实邮箱 -->
- 💬 GitHub Issues：欢迎提出建议与反馈

---

## 📄 License

本项目采用 MIT 协议，详情请见 [LICENSE](./LICENSE) 文件。
