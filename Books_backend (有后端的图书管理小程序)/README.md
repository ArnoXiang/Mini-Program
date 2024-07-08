# 书籍管理小程序（含后端）

这是一个简单的整合了前后端的书籍管理小程序demo，用户可以添加书籍并查看当前书籍和历史添加的书籍。

## 功能

- 查看当前书籍
- 查看历史添加书籍
- 添加新书籍


## 使用技术

### 前端

- **微信小程序**：用于构建用户界面。
- **WXML**：用于描述页面结构。
- **WXSS**：用于页面样式设计。
- **JavaScript**：用于页面逻辑和数据处理。
- **微信小程序API**：用于与后端进行数据交互。

### 后端

- **FastAPI**：用于构建后端API服务。
- **Pydantic**：用于数据验证和序列化。
- **Uvicorn**：用于运行ASGI服务器。

## 安装与使用

### 前端

1. 克隆仓库到本地：

    ```bash
    git clone https://github.com/yourusername/book-management-miniapp.git
    ```

2. 使用微信开发者工具打开项目。

3. 确保 `app.js`、`app.json` 和 `app.wxss` 文件存在并正确配置。

### 后端

1. 安装 FastAPI 和 Uvicorn：

    ```bash
    pip install fastapi uvicorn
    ```

2. 创建并运行后端服务：

    ```bash
    uvicorn main:app --reload
    ```

### 配置前端请求

确保前端请求的URL指向后端服务。

## 截图
<img width="301" alt="展示页" src="https://github.com/ArnoXiang/Mini-Program/assets/100560218/cf91d49e-73ef-4830-a359-b5e22ff43938">

<img width="298" alt="添加页" src="https://github.com/ArnoXiang/Mini-Program/assets/100560218/1dc275b1-2319-48cb-a00a-d675bec77837">



