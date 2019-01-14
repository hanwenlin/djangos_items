### 一、项目概述  
### 项目运行环境
  1. Python3.6+
  2. Django 1.11
  3. MySQL 5.7
  4. 其他插件(图片处理、分页、验证码....)
  
### 项目详细功能介绍
#### 前台功能
  1. 项目首页展示
  2. 轮播图
  3. 博客推荐
  4. 最新发布
  5. 博客分类
  6. 最新评论文章
  7. widgets小插件
  8. 搜索功能
  9. 博客分类功能
  10. 博客标签查询
  11. 友情链接
  12. 博客分页功能
  13. 博客详细
  14. 最新评论文章
  15. 发表评论
  16. 评论展示
  17. 评论数阅读数
  18. 登录注册功能
  19. 邮箱验证功能
  20. 注销功能
  21. 页面模板
  22. 标签云功能
  23. 读者墙功能
  
#### 后台功能
  1. 用户维护
  2. 权限管理
  3. 博客分类维护
  4. 标签维护
  5. 友情链接
  6. 轮播图维护
  
#### 项目演示

#### 二、开发环境搭建
> 使用virtualenv 和 virtualenwrapper
1. Mysql
sudo apt install mysql-server mysql-client
2. 安装mysql驱动
pip install pymysql     //使用时经常需要在__Init__文件中加入as mysql啥的
3. 安装django
pip install django=2.1

### 创建项目
#### 创建项目和应用
创建项目：  
`django-admin startproject django_blog`
创建app:  
`python3 manage.py startapp userapp`
`django-admin startapp blogapp`

#### 配置数据库
+ 在settings文件中数据库

#### 创建数据库（执行迁移文件）
`python manage.py migrate`
  + 错误1：django.core.exceptions.ImproperlyConfigured: Error loading MySQLdb module.  Did you install mysqlclient?  
    解决： Django安装目录下 __init__.py 文件中加入 import pymysql  pymysql.install_as_MySQLdb()  
    安装目录在：C:\Users\28277\AppData\Local\Programs\Python\Python36\Lib\site-packages\django
  + 错误2： django.db.utils.InternalError: (1049, "Unknown database 'django_blog_db'")  
    settings数据库配置中有'NAME': 'django_blog_db',说明这个库名字。但是我后面对应的mysql里面没有这个库，需要建这个库，create database django_blog_db
    

#### 创建超级管理员
`python3 manage.py createsuperuser`


### 创建数据模型
#### USERAPP
##### USER(用户模型)  Email验证模型  
      见userapp里面的models.py  E:\Python_learn\django_blog\userapp\models.py
> 提示：需要在settings配置文件中设置:AUTH_USER_MODEL = 'users.BlogUser'

#### BLOGAPP
#### Banner(轮播图模型)  Category(博客分类模型) Tags(标签模型)  Blog(博客模型) Comment(评论模型) FriendlyLink(友情链接模型)
    见Blogapp中的models.py    E:\Python_learn\django_blog\blogapp\models.py
    
  
### 五、实现首页页面模板
#### 创建模板文件夹
#### 配置静态文件路径
> 创建模板文件templates,静态文件路径static,并在settings.py中设置

    
 



    
  





  
