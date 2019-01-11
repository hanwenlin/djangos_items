#### 1、django是否安装以及版本
  python -m django --version  
安装了以后查看django版本
```  script
python
import django
django.get_version()```

#### 2、安装
python -m pip install django==2.1.5  


#### 3、创建项目及创建app
    1. 创建项目  django-admin startproject mysite               //This will create a mysite directory in your current directory
    ** 注意**
    项目名，不要冲突，比如django,python，或者包名test.其实就是和函数命名规则差不多
