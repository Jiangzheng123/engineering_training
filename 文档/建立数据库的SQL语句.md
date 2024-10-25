```sql
// 创建并使用数据库
create database blog;
use blog;

// 创建用户表
create table user
(
    id           int auto_increment comment '用户id'
        primary key,
    account      varchar(20)                         not null comment '用户账号',
    nickname     varchar(20)                         not null comment '用户昵称',
    image_id     int                                 null comment '头像id，与image表的主键对应',
    password     varchar(20)                         not null comment '用户密码',
    type         int                                 not null comment '用户类型，0为管理者，1为普通用户，2为付费用户',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可'
)
    comment '用户表';

// 创建文章表
create table article
(
    id           int auto_increment comment '文章id'
        primary key,
    title        varchar(40)                         not null comment '文章标题',
    introduction varchar(200)                        null comment '文章简介',
    content      text                                null comment '文章文本内容',
    version      int       default 1                 not null comment '文章版本号，默认为1',
    browse_num   int       default 0                 not null comment '浏览数，默认为0',
    comment_num  int       default 0                 not null comment '评论数，默认为0',
    like_num     int       default 0                 not null comment '点赞数，默认为0',
    share_num    int       default 0                 not null comment '分享数，默认为0',
    heat         double    default 0                 not null comment '热度，默认为0',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可'
)
    comment '文章表';

// 创建标签表
create table label
(
    id           int auto_increment comment '标签id'
        primary key,
    name         varchar(10)                         not null comment '标签名字',
    description  varchar(50)                         null comment '标签描述',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可'
)
    comment '标签表';

// 创建文章与标签的对应表
create table article_label
(
    article_id   int                                 not null comment '文章id',
    label_id     int                                 not null comment '标签id',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可',
    constraint article_label_pk
        primary key (article_id, label_id)
)
    comment '文章与标签的对应表';

// 创建图像表
create table image
(
    id           int auto_increment comment '图像id'
        primary key,
    type         int                                 not null comment '图像类型，0代表用户头像，1代表文章配图',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可'
)
    comment '图像表';

// 创建网站信息表
create table web_info
(
    name            varchar(20)  not null comment '网站名称',
    description     varchar(200) null comment '网站描述',
    article_content text         null comment '介绍文章文本内容'
)
    comment '网站信息表';

// 创建里程碑表
create table blog.milestones
(
    id           int auto_increment comment '里程碑id'
        primary key,
    name         varchar(20)                         not null comment '事件名',
    description  varchar(50)                         null comment '事件描述',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可'
)
    comment '里程碑表';

// 创建系统日志表
create table log
(
    id           int auto_increment comment '日志id'
        primary key,
    people       varchar(20)                         not null comment '操作发起者的用户名',
    type         int                                 not null comment '操作发起者的类型，0为管理员，1为普通用户，2为付费用户',
    address      varchar(40)                         not null comment '操作发起者的网络ip地址',
    description  varchar(100)                        not null comment '操作描述',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可'
)
    comment '系统日志表';

// 公告表暂不创建

// 创建评论表
create table comment
(
    id           int auto_increment comment '主键'
        primary key,
    name         varchar(20)                         not null comment '评论人昵称',
    email        varchar(30)                         not null comment '评论人邮箱',
    content      varchar(100)                        not null comment '评论内容',
    reply_id     int       default 0                 not null comment '回复的评论id，0表示不是回复',
    created_time timestamp default CURRENT_TIMESTAMP not null comment '创建时间，由MySQL自动填充即可'
)
    comment '评论表';
```

