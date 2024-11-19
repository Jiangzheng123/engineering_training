```
server
├── .mvn                          # Maven库
├── src                           # 源代码文件夹
│   ├── main
│   │   └── java
│   │       └── com.server
│   │           ├── common
│   │           │   ├── BaseContext.java         # 基础上下文类
│   │           │   ├── Constants.java           # 常量类
│   │           │   └── Result.java              # 结果封装类
│   │           ├── config
│   │           │   ├── CorsConfig.java          # 跨域资源共享配置类
│   │           │   ├── MybatisPlusConfig.java   # MyBatis Plus配置类
│   │           │   ├── SwaggerConfig.java       # Swagger配置类
│   │           │   └── WebConfig.java           # Web配置类
│   │           ├── controller
│	│           │   ├── dto
│	│           │   │   ├── CommentDTO.java          # 评论数据传输对象
│	│           │   │   ├── LikeDTO.java             # 点赞数据传输对象
│	│           │   │   ├── LoginDTO.java            # 登录数据传输对象
│	│           │   │   └── UserInfoDTO.java         # 用户信息数据传输对象
│	│           │   ├── vo
│	│           │   │   ├── ArticleChartVO.java      # 文章图表视图对象
│	│           │   │   ├── ArticleListVO.java       # 文章列表视图对象
│	│           │   │   ├── ArticleVO.java           # 文章视图对象
│	│           │   │   ├── CommentChartVO.java      # 评论图表视图对象
│	│           │   │   ├── CommentVO.java           # 评论视图对象
│	│           │   │   ├── ImageListVO.java         # 图片列表视图对象
│	│           │   │   ├── LabelListVO.java         # 标签列表视图对象
│	│           │   │   ├── LoginVO.java             # 登录视图对象
│	│           │   │   ├── OverviewVO.java          # 概览视图对象
│	│           │   │   ├── UploadingVO.java         # 上传视图对象
│	│           │   │   └── UserInfoVO.java          # 用户信息视图对象
│   │           │   ├── ArticleController.java   # 文章相关功能业务流程控制
│   │           │   ├── CommentController.java   # 评论相关功能业务流程控制
│   │           │   ├── HomeController.java      # 首页相关功能业务流程控制
│   │           │   ├── ImageController.java     # 图片相关功能业务流程控制
│   │           │   ├── LabelController.java     # 标签相关功能业务流程控制
│   │           │   ├── LogController.java       # 日志相关功能业务流程控制
│   │           │   ├── MilestonesController.java# 里程碑相关功能业务流程控制
│   │           │   ├── UserController.java      # 用户相关功能业务流程控制
│   │           │   └── WebInfoController.java   # 网站信息相关功能业务流程控制
│   │           ├── entity
│   │           │   ├── Article.java             # article表的实体类数据模型
│   │           │   ├── Comment.java             # comment表的实体类数据模型
│   │           │   ├── Image.java               # image表的实体类数据模型
│   │           │   ├── Label.java               # label表的实体类数据模型
│   │           │   ├── Log.java                 # log表的实体类数据模型
│   │           │   ├── Milestones.java          # milestones表的实体类数据模型
│   │           │   ├── User.java                # user表的实体类数据模型
│   │           │   └── WebInfo.java             # webinfo表的实体类数据模型
│   │           ├── exception
│   │           │   ├── GlobalExceptionHandler.java # 全局异常处理类
│   │           │   └── MyException.java            # 自定义异常类
│   │           ├── interceptor
│   │           │   └── JwtTokenInterceptor.java # JWT令牌拦截器类
│   │           ├── mapper
│   │           │   ├── ArticleLabelMapper.java  # article_label表（文章标签表）数据访问对象
│   │           │   ├── ArticleMapper.java       # article表（文章表）数据访问对象
│   │           │   ├── CommentMapper.java       # comment表（评论表）数据访问对象
│   │           │   ├── ImageMapper.java         # image表（图片表）数据访问对象
│   │           │   ├── LabelMapper.java         # label表（标签表）数据访问对象
│   │           │   ├── LogMapper.java           # log表（日表）数据访问对象
│   │           │   ├── MilestonesMapper.java    # milestones表（里程碑表）数据访问对象
│   │           │   ├── UserMapper.java          # user表（用户表）数据访问对象
│   │           │   └── WebInfoMapper.java       # webinfo表（网站信息表）数据访问对象
│   │           ├── properties
│   │           │   └── JwtProperties.java       # JWT属性配置类
│   │           ├── service
│   │           │   ├── impl
│   │           │   │   ├── ArticleLabelServiceImpl.java # 文章标签数据处理业务逻辑
│   │           │   │   ├── ArticleServiceImpl.java      # 文章数据处理业务逻辑
│   │           │   │   ├── CommentServiceImpl.java      # 评论数据处理业务逻辑
│   │           │   │   ├── ImageServiceImpl.java        # 图片数据处理业务逻辑
│   │           │   │   ├── LabelServiceImpl.java        # 标签数据处理业务逻辑
│   │           │   │   ├── LogServiceImpl.java          # 日志数据处理业务逻辑
│   │           │   │   ├── MilestonesServiceImpl.java   # 里程碑数据处理业务逻辑
│   │           │   │   ├── UserServiceImpl.java         # 用户数据处理业务逻辑
│   │           │   │   └── WebInfoServiceImpl.java      # 网站信息数据处理业务逻辑
│   │           │   ├── IArticleService.java             # 文章数据处理方法声明接口
│   │           │   ├── ICommentService.java             # 评论数据处理方法声明接口
│   │           │   ├── IImageService.java               # 图片数据处理方法声明接口
│   │           │   ├── ILabelService.java               # 标签数据处理方法声明接口
│   │           │   ├── ILogService.java                 # 日志数据处理方法声明接口
│   │           │   ├── IMilestonesService.java          # 里程碑数据处理方法声明接口
│   │           │   ├── IUserService.java                # 用户数据处理方法声明接口
│   │           │   └── IWebInfoService.java             # 网站信息数据处理方法声明接口
│   │           ├── util
│   │           │   ├── JwtUtils.java                    # JWT工具类
│   │           │   ├── RedisCache.java                  # Redis缓存工具类
│   │           │   └── UploadUtils.java                 # 上传工具类
```

