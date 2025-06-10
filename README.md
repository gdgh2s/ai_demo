# 一、项目简介

本项目是一个基于 Python 的 AI 助手服务，提供用户注册、会话初始化以及与 AI 助手进行流式对话的功能。

- **后端**：使用了 FastAPI 框架，结合数据库操作实现用户管理和会话管理。
- **前端**：使用了 Vue 框架，使用 ElementUI 构架界面。

## 二、后端

### 后端各目录功能说明

1. **auth**：授权相关模块，包含访问令牌生成和用户密码处理的代码。
   - `access_token.py`：负责生成访问令牌。
   - `user_passwd.py`：处理用户密码的哈希和验证。

2. **bin**：主要执行文件目录。
   - `main.py`：项目的入口文件，定义了 FastAPI 应用和 API 路由。

3. **config**：配置加载模块。
   - `init_dotenv.py`：初始化环境变量。
   - `log_config.py`：日志配置文件。

4. **db**：数据库相关模块。
   - `chat_messages.py`：处理聊天消息的数据库操作。
   - `chat_session.py`：处理聊天会话的数据库操作。
   - `sql_engine.py`：数据库引擎配置。
   - `sql_init.py`：数据库初始化脚本。
   - `sql_test.py`：数据库测试脚本。
   - `user.py`：处理用户信息的数据库操作。

5. **function**：聊天功能模块。
   - `chat.py`：实现聊天功能的核心逻辑。

6. **project.env**：dotenv 环境变量配置文件，用于存储敏感信息和配置参数。

### 安装依赖

```bash
pip install -r requirements.txt
```

### 启动命令

```bash
uvicorn /bin/main.py --reload --host 0.0.0.0 --port 8088
```

**注意事项**

- 请确保 project.env 文件中的配置参数正确，特别是数据库连接信息和密钥。
- 生产环境中建议关闭 --reload 参数以提高性能。
- 定期备份数据库以防止数据丢失。

## 三、前端

前端朋友写的，具体实现不了解。

### 安装依赖

```bash
npm i
```

### 启动命令

```bash
npm run dev
```

