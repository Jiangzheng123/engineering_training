```
client/
│
├── node_modules/           # 项目依赖包目录
├── public/    
├── src/                    # 源代码文件夹
│   ├── api/
│   │   └── article.js      # 文章相关的API请求
│   ├── assets/             # 静态资源文件夹
│   ├── components/         # 公共组件
│   │   ├── ArticleList.vue  # 文章列表组件
│   │   ├── CommentList.vue   # 评论列表组件
│   │   ├── CommentSection.vue  # 评论区组件
│   │   ├── Header.vue       # 网站头部导航组件
│   │   ├── TagFilter.vue   # 标签筛选组件
│   │   └── thumb-up.vue    # 点赞按钮组件
│   ├── router/
│   │   └── index.js        # 路由配置文件
│   ├── utils/
│   │   └── request.js      # 工具类函数，如HTTP请求封装
│   ├── views/              # 页面视图组件
│   │   ├── HomeView.vue    # 博客欢迎页
│   │   ├── AboutView.vue   # 关于页面
│   │   ├── DetailView.vue  # 文章详情页
│   │   └── PostView.vue    # 文章列表页
│   ├── App.vue             # 主应用组件
│   └── main.js             # 应用入口文件
│
├── package-lock.json       # 锁定依赖版本文件
├── package.json            # 项目依赖说明文件
├── README.md               # 项目说明文档
└── vue.config.js           # Vue项目的配置文件
```

