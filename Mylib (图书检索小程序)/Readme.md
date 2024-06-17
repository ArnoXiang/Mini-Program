## 截至202405：
- 因没有服务器和数据库，图鉴的数据都放在了data文件夹的各js文件中，因此文件体积较大，考虑之后上传云相册，把链接放在js中处理；
- “发现”中的数据均来自豆瓣api，现暂时无法访问，需解决；
- 基本功能与代码框架（包括目录的分层：图书类别 --> 作家地区 --> 具体书目 --> 详细信息陈列）已完成，图书内容等待后续补充。
- 做个梦：做国际化，添加中英双语切换功能 (✪ω✪)

## 202406:
- 使用聚合数据调取图书榜单失败，需解决；
- 将“发现”页暂更改为个人信息页，展示内容为“个人信息”、“个人推荐图书展示”

## 文件目录框架
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
│   │   ├── star/
│   │   │   ├── star-template.wxml
│   │   │   └── star-template.wxss
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
