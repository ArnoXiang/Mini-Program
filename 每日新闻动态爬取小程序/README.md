# 项目简介
一个每日新闻动态爬取微信小程序，为期末小组项目做准备时单独开发，通过对聚合数据（www.juhe.cn）

提供的每日新闻头条进行爬取，返回的内容包括新闻的主要内容，同时设置WebView页面，实现在用户点击相应新闻后，对新闻的全部内容进行展示。

## 主要功能

1. **首页**：展示基本的欢迎信息和导航。
2. **日志页面**：展示用户操作日志。
3. **新闻页面**：展示最新的新闻内容。
4. **WebView 页面**：嵌入外部网页内容。

## 目录结构

```
integrate_news/
├── app.js              // 小程序入口文件
├── app.json            // 小程序全局配置文件
├── app.wxss            // 小程序全局样式文件
├── pages/              // 页面目录
│   ├── index/          // 首页
│   │   ├── index.js
│   │   ├── index.wxml
│   │   ├── index.wxss
│   │   └── index.json
│   ├── logs/           // 日志页面
│   │   ├── logs.js
│   │   ├── logs.wxml
│   │   ├── logs.wxss
│   │   └── logs.json
│   ├── news/           // 新闻页面
│   │   ├── news.js
│   │   ├── news.wxml
│   │   ├── news.wxss
│   │   └── news.json
│   └── webview/        // WebView 页面
│       ├── webview.js
│       ├── webview.wxml
│       ├── webview.wxss
│       └── webview.json
└── utils/              // 工具函数目录
    └── util.js
