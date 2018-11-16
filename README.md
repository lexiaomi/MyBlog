# MyBlog
个人博客系统
本系统源码地址在：
https://github.com/lexiaomi/MyBlog
1.首先同在本地的git下载，命令：
git clone https://github.com/lexiaomi/MyBlog
2.在下载到本地的目录建立虚拟环境：
python3 -m venv venvname
进入venvname目录激活虚拟环境：
source bin/activate(Linux下)
 3.安装项目所需的环境依赖库：
 pip install requirements.txt
 
 4.配置数据库，在settings.py文件：
 DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'Blog',
        'USER': 'root',
        'PASSWORD': 'root',
        'HOST': 'localhost',
        'PORT': '3306',
        'CHARSET': 'utf8',
    }
}
不是MySQL数据库请配置其他数据库

 5. 进行数据库迁移：
	python manage.py makemigrations blog
	python manage.py migrate 
	
6. 创建用户：
	python manage.py createsuperuser 
	
7. 运行本系统：
	python manage.py runserver 
