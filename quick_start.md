# django入门
## 创建项目
命令行如下：`django-admin startproject mysite` 其中mysite为项目的名称
### 运行项目
运行项目的命令行如下：`python manage.py runserver`
运行时项目时可以指定地址：`python manage.py runserver 0:8080` ，
其中0代表`0.0.0.0`,也可以指定具体的IP地址。
### 创建app
命令行为：`python manage.py startapp polls` 其中polls为app的名称

### 路径匹配
```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('polls/', include('polls.urls')),
    path('admin/', admin.site.urls),
]
```

项目中的每一个urls文件中存储的是路由，函数[path()](https://docs.djangoproject.com/en/2
.2/ref/urls/#django.urls.path)的用途如下：   
```python

```
函数[re_path()](https://docs.djangoproject.com/en/2.2/ref/urls/#django.urls
.re_path)的用途如下：

## part1
讲述如何创建项目
```
django-admin startproject projectname
```

如何启动服务
```
python manage.py runserver
python manage.py runserver 0:8000
python manage.py runserver 8000
```

创建app
```
python manage.py startapp appname
```


## part 2
简单的讲述如何进行django的数据库的配置，包括支持的数据库引擎，详情间[databases](https://docs.djangoproject.com/en/2.2/ref/databases/#third-party-notes)

在setting.py的配置文件中的INSTALLED_APPS中列举了在当前的Django项目中已经
激活的应用。

### 创建model和数据库迁移
django中继承子 django.db.models.Model的类为数据模型类，使用用于创建在INSTALLED_APPS中
列举的应用的相关的数据库表
```
python manage.py migrate
```

使用一下命令记录app的数据库变更
```
python manage.py makemigrations mypp
```

使用改命令执行app的数据变更
```
python manage.py sqlmigrate polls 0001
```

### 命令行
```
> python manage.py shell

>>> from polls.models import Choice, Question  # Import the model classes we just wrote.

# No questions are in the system yet.
>>> Question.objects.all()
```

### 创建管理员超级用户
```
python manage.py createsuperuser
```
在本地的http://127.0.0.1:8000/admin/登陆管理员用户






