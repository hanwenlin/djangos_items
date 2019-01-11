#### 1、django是否安装以及版本
  python -m django --version  
安装了以后查看django版本
(```)python
import django
django.get_version()
(```)
#### 2、安装
python -m pip install django==2.1.5  


#### 3、创建项目及创建app
    1. 创建项目  django-admin startproject mysite               //This will create a mysite directory in your current directory
    **注意**  项目名，不要冲突，比如django,python，或者包名test.其实就是和函数命名规则差不多  
    2. [目录结构]('https://github.com/hanwenlin/djangos_items/blob/master/django_project_%E7%BB%93%E6%9E%84.jpg')
     + The outer mysite/ root directory只是项目的一个容器，不重要，可以随便改名
     + manage.py: 命令行工具，可以与django项目进行交互 python manage.py startapp ...
     + The inner mysite/ directory is the actual Python package for your project.这个名字经常作为包名导入
     + mysite/__init__.py: An empty file 告诉这是一个python包，里面可以放入doc文档
     + mysite/settings.py: Settings/configuration for this Django project.
     + mysite/urls.py: The URL declarations for this Django project  总的路由系统，经常导入很多app的路由系统
     + mysite/wsgi.py: An entry-point for WSGI-compatible web servers to serve your project.服务器部署
    
      
