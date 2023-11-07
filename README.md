# Nobibi-api
基于node express mongo 开发的Nobibi接口部分

## 项目运行
> 项目运行前请保证已经安装以下应用及环境
> node (>=8.0.0)
> mongo

1. Clone项目
```
git clone https://github.com/ioaty/Nobibi-api.git nobibi-api
```

2. 安装依赖
```
cd nobibi-api
npm install 或 yarn
```

3. 导入mongo基础数据
```
mongorestore -d Nobibi /你的项目目录/db/Nobibi/
```

4. 运行项目
```
npm run start
```


## 项目部署
> 项目运行前请保证已经安装以下应用及环境
> node (>=8.0.0)
> mongo

1. 将项目上传到ssh

2. cd到项目目录，安装依赖
```
cd my-porject
npm install 或 yarn
```
3. 导入mongo基础数据
```
mongorestore -d Nobibi /你的/项目/目录/db/lib/Nobibi/
```

4. 运行pm2
```
npm run pm2
```

## 功能模块

- [x] 用户管理
- [x] 角色管理
- [x] 内容管理
- [x] 评论管理
- [x] 内容分类管理

## 目录结构

``` lua
├── config/               # 设置目录
├── logs/               # log目录
├── lib/               # 核心代码
│ ├── controller/       # 组件目录
│ │ ├── categorytController.js       # 分类模块
│ │ ├── commentController.js         # 评论模块
│ │ ├── roleController.js            # 角色模块
│ │ ├── topicController.js           # 内容模块
│ │ ├── userController.js            # 用户模块
│ ├── models/       # mongo模型目录
│ │ ├── category.js       # 分类mongo模型
│ │ ├── comment.js         # 评论mongo模型
│ │ ├── role.js            # 角色mongo模型
│ │ ├── topic.js           # 内容mongo模型
│ │ ├── user.js            # 用户mongo模型
│ ├── prototype/   
│ │ ├── baseComponent.js            # 通用组件
├── routes/               # api路由目录
├── utils/               # 通用方法
├── .babelrc           # babel配置
├── app.js             # 项目启动模块
├── index.js           # 项目启动入口
└──  package.json       # 项目信息

```

## 技术选型

- koa2 - [https://koajs.com/](https://koajs.com/)
- koa-jwt - [https://github.com/koajs/jwt](https://github.com/koajs/jwt)
- babel - [https://babeljs.io/](https://babeljs.io/)
- mongoose - [https://mongoosejs.com/](https://mongoosejs.com/)
- redis（选用，session鉴权）
- nodemon
- pm2

## 更新日志
2019-7-24 更新到v2.0.0 使用koa重构 鉴权改为token验证
2019-7-12 更新到v1.1.0 升级babel7 重构部分代码 需重新安装npm依赖包
