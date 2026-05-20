<h1 align="center">
    学校管理系统 (School Management System)
</h1>

<h3 align="center">
    一个基于 MERN 技术栈的高效学校管理解决方案，旨在简化学校管理、班级组织以及师生之间的沟通。
</h3>

---

## **项目介绍**

本项目是一个功能完善的学校管理系统，采用 MERN（MongoDB, Express.js, React.js, Node.js）技术栈开发。系统通过为管理员、教师和学生提供不同的角色权限，实现了从学生入学、考勤管理到成绩评估的全流程数字化管理。

## **核心功能**

- **多角色支持：** 系统支持管理员 (Admin)、教师 (Teacher) 和学生 (Student) 三种角色，每种角色拥有独立的控制面板。
- **管理员端：** 管理班级、科目、教师及学生，查看投诉建议，发布通知公告。
- **教师端：** 管理考勤（签到/缺勤）、录入学生成绩、查看个人资料及班级信息。
- **学生端：** 查看个人课程、成绩单、考勤统计（通过图表展示），查看通知并提交建议。
- **数据可视化：** 集成图表展示学生的出勤率和成绩表现，直观反映学习状态。
- **即时通知：** 系统内的通知系统确保重要信息能快速传达给所有师生。

## **技术栈**

- **前端：** React.js, Material UI, Redux Toolkit, Axios, Recharts (数据可视化)
- **后端：** Node.js, Express.js
- **数据库：** MongoDB (Mongoose)
- **状态管理：** Redux

---

## **项目架构**

```text
School-Management-System/
├── backend/                # 后端代码 (Node.js/Express)
│   ├── controllers/        # 业务逻辑处理
│   ├── models/             # MongoDB 数据模型 (Mongoose)
│   ├── routes/             # API 路由定义
│   └── index.js            # 服务端入口
├── frontend/               # 前端代码 (React)
│   ├── src/
│   │   ├── components/     # 通用组件
│   │   ├── pages/          # 页面组件 (Admin/Teacher/Student)
│   │   ├── redux/          # Redux 状态管理逻辑
│   │   └── App.js          # React 路由与应用入口
│   └── package.json        # 前端依赖配置
└── README.md               # 项目文档
```

---

## **快速启动**

### **1. 克隆项目**

```bash
git clone https://github.com/Yogndrr/MERN-School-Management-System.git
cd School-Management-System
```

### **2. 后端配置**

1. 进入后端目录：
   ```bash
   cd backend
   ```
2. 安装依赖：
   ```bash
   npm install
   ```
3. 创建 `.env` 文件并配置环境变量：
   ```env
   MONGO_URL = mongodb://127.0.0.1:27017/sms  # 你的 MongoDB 连接地址
   SECRET_KEY = your_secret_key               # 随意填写，用于 JWT 加密
   ```
4. 启动后端服务：
   ```bash
   npm start
   ```
   后端服务默认运行在 `http://localhost:5000`。

### **3. 前端配置**

1. 打开新的终端，进入前端目录：
   ```bash
   cd frontend
   ```
2. 安装依赖：
   ```bash
   npm install
   ```
3. 创建 `.env` 文件并配置：
   ```env
   REACT_APP_BASE_URL = http://localhost:5000
   ```
4. 启动前端应用：
   ```bash
   npm start
   ```
   前端应用默认运行在 `http://localhost:3000`。

---

## **部署说明**

### **后端部署 (Render 示例)**
1. 将代码推送到 GitHub。
2. 在 Render 中创建新的 Web Service。
3. 设置 Root Directory 为 `backend`。
4. Build Command: `npm install`
5. Start Command: `npm start`
6. 在环境变量中添加 `MONGO_URL` 和 `SECRET_KEY`。

### **前端部署 (Netlify 示例)**
1. 将代码推送到 GitHub。
2. 在 Netlify 中关联仓库。
3. 设置 Base Directory 为 `frontend`。
4. Build Command: `npm run build`
5. Publish Directory: `frontend/build`
6. 在环境变量中设置 `REACT_APP_BASE_URL` 指向已部署的后端地址。

---

## **贡献与反馈**

欢迎通过 Issue 或 Pull Request 为本项目做出贡献！如果您觉得这个项目有帮助，请给一个 ⭐️！
