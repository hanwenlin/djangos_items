1. question1:django.db.migrations.exceptions.InconsistentMigrationHistory: Migration admin.0001_initial is applied before its d
ependency users.0001_initial on database 'default'.  
answer: 删除数据库中 除了auth_user的其他表，然后重新来一次 大概原因是因为admin的模型依赖了之前默认的user模型吧  

2. questions: python manage.py makemigrations  No changes detected django.db.utils.OperationalError: (1060, "Duplicate column name 'XXX')
answer: 删除掉app目录下migrations目录下的0001_initial.py 删除数据库里面的表格，因为重复了，就是没啥变化

3. questions: TypeError: __init__() missing 1 required positional argument: 'on_delete'
answer: 在括号内加入属性on_delete=models.CASCADE即可   course = models.ForeignKey(Course,verbose_name='课程',on_delete=models.CASCADE)

4. django 2.1以上版本使用的xadmin  https://github.com/sshwsfc/xadmin/tree/django2  
pip install git+git://github.com/sshwsfc/xadmin.git  
