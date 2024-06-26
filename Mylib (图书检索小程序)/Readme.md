## 截至202405：

- 因没有服务器和数据库，图鉴的数据都放在了data文件夹的各js文件中，因此文件体积较大，考虑之后上传云相册，把链接放在js中处理；
- “发现”中的数据均来自豆瓣api，现暂时无法访问，需解决；
- 基本功能与代码框架（包括目录的分层：图书类别 --> 作家地区 --> 具体书目 --> 详细信息陈列）已完成，图书内容等待后续补充。
- 做个梦：做国际化，添加中英双语切换功能 (✪ω✪)

## 截至202406:

- 使用聚合数据调取图书榜单失败，需解决；
- 将“发现”页暂更改为个人信息页，展示内容为“个人信息”、“个人推荐图书展示”
- 新增“评价”功能，用户可以在图书简介下上传/删除自己的评价，最终评价会展示在图书相关信息下
- 新增“展示书架”功能，用户可以上传/删除自己喜欢的图书的封面、书名、作者等相关信息，最终所有内容均会展示在“我的”页面中
- 新增微信用户登录功能

## 一、简介

该图书展示微信小程序旨在提供一个简洁直观的界面，帮助用户发现和了解不同类别的书籍的基本信息，同时用户也可以对自己的图书馆进行展示与自定义。小程序通过本地数据存储图书信息，并支持按类别、作家地区和具体书目的层级进行浏览，同时也支持用户进行评价与个人页面修改等基本交互功能。

## 二、主要功能

### 图书分类展示

图书类别：畅销书、小说类、文学类、历史类、经济类、工具类等。
数据存储在 data 文件夹中，通过各 js 文件进行管理。
图书详细信息

点击图书类别后，展示作家地区及具体书目。
提供详细的图书信息展示页面。
交互：用户可以在图书简介下输入自己的评价，最终评价会展示在图书相关信息下

个人信息页

展示用户的个人信息及推荐书籍（现为“发现”页的临时替代）。
用户可以上传/删除自己喜欢的图书的封面、书名、作者等相关信息，最终所有内容将会展示在“我的”页面中

## 三、文件目录框架

```
Mylib/
│
├── data/
│   ├── family.js
│   ├── gens.js
│   └── spes.js
│
├── img/
│   └── family/ (图书类别图片)
│
├── pages/
│   ├── books/
│   │   ├── book/
│   │   │   ├── book-template.wxml
│   │   │   └── book-template.wxss
│   │   ├── books.js
│   │   ├── books.json
│   │   ├── books.wxml
│   │   └── books.wxss
│   │
│   ├── detail/
│   │   ├── detail.js
│   │   ├── detail.json
│   │   ├── detail.wxml
│   │   └── detail.wxss
│   │
│   ├── family-item/
│   │   ├── family-item-template.wxml
│   │   └── family-item-template.wxss
│   │
│   ├── genus/
│   │   ├── genus.js
│   │   ├── genus.json
│   │   ├── genus.wxml
│   │   └── genus.wxss
│   │
│   ├── species/
│   │   ├── species.js
│   │   ├── species.json
│   │   ├── species.wxml
│   │   └── species.wxss
│   │
│   ├── tujian-family/
│   │   ├── tujian-family.js
│   │   ├── tujian-family.json
│   │   ├── tujian-family.wxml
│   │   └── tujian-family.wxss
│   │
│   ├── welcome/
│   │   ├── welcome.js
│   │   ├── welcome.json
│   │   ├── welcome.wxml
│   │   └── welcome.wxss
│
├── utils/
│   └── utils.js
│
├── app.js
├── app.json
├── app.wxss
├── project.config.json
├── project.private.config.json

```
