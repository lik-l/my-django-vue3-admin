# Django-Vue3-Admin



## 给框架点赞

<div style="display: flex; gap: 10px;">
 <img src='https://django-vue-admin.com/alipay.jpg' width='200'>
 <img src='https://django-vue-admin.com/wechat.jpg' width='200'>
</div>


## 源码地址

github地址：[https://github.com/huge-dream/django-vue3-admin](https://github.com/huge-dream/django-vue3-admin)👩‍👦‍👦

## 准备工作
~~~
Python >= 3.12.0 
nodejs >= 16.0
Mysql >= 8.0
Redis 

## 前端♝

```bash
# 克隆项目
git clone https://gitee.com/huge-dream/django-vue3-admin.git

# 进入项目目录
cd web

# 安装依赖
npm install yarn
yarn install --registry=https://registry.npmmirror.com

# 启动服务
yarn build
# 浏览器访问 http://localhost:8080
# .env.development 文件中可配置启动端口等参数
# 构建生产环境
# yarn run build
```



## 后端💈

~~~bash
1. 进入项目目录 cd backend
2. 在项目根目录中，复制 ./conf/env.example.py 文件为一份新的到 ./conf 文件夹下，并重命名为 env.example.py
3. 在 env.example.py 中配置数据库信息
	mysql数据库版本建议：8.0
	mysql数据库字符集：utf8mb4
4. 安装依赖环境
	pip3 install -r requirements.txt
5. 执行迁移命令：
	python3 manage.py makemigrations
	python3 manage.py migrate
6. 初始化数据
	python3 manage.py init
7. 初始化省市县数据:
	python3 manage.py init_area
8. 启动项目
	python3 manage.py runserver 0.0.0.0:8000
或使用 uvicorn :
  uvicorn application.asgi:application --port 8000 --host 0.0.0.0 --workers 8
~~~
## 开发建议
前后端backend与web各自单独一个窗口打开进行开发

### 访问项目

- 访问地址：[http://localhost:8080](http://localhost:8080) (默认为此地址，如有修改请按照配置文件)
- 账号：`superadmin` 密码：`admin123456`





### docker-compose 运行

~~~shell
# 先安装docker-compose (自行百度安装),执行此命令等待安装，如有使用celery插件请打开docker-compose.yml中celery 部分注释
docker-compose up -d
# 初始化后端数据(第一次执行即可)
docker exec -ti dvadmin3-django bash
python manage.py makemigrations 
python manage.py migrate
python manage.py init_area
python manage.py init
exit

前端地址：http://127.0.0.1:8080
后端地址：http://127.0.0.1:8080/api
# 在服务器上请把127.0.0.1 换成自己公网ip
账号：superadmin 密码：admin123456

# docker-compose 停止
docker-compose down
#  docker-compose 重启
docker-compose restart
#  docker-compose 启动时重新进行 build
docker-compose up -d --build
~~~



## 演示图✅

![image-01](https://foruda.gitee.com/images/1701348994587355489/1bc749e7_5074988.png)

![image-02](https://foruda.gitee.com/images/1701349037811908960/80d361db_5074988.png)

![image-03](https://foruda.gitee.com/images/1701349224478845203/954f0a7b_5074988.png)

![image-04](https://foruda.gitee.com/images/1701349248928658877/64926724_5074988.png)

![image-05](https://foruda.gitee.com/images/1701349259068943299/1306ba40_5074988.png)

![image-06](https://foruda.gitee.com/images/1701349294894429495/e3b3a8cf_5074988.png)

![image-07](https://foruda.gitee.com/images/1701350432536247561/3b26685e_5074988.png)

![image-08](https://foruda.gitee.com/images/1701350455264771992/b364c57f_5074988.png)

![image-09](https://foruda.gitee.com/images/1701350479266000753/e4e4f7c5_5074988.png)

![image-10](https://foruda.gitee.com/images/1701350501421625746/f8dd215e_5074988.png)

## 审批流插件

![输入链接说明](https://bbs.django-vue-admin.com/uploads/20250321/97fbbf29673edfd66a1edd49237791bb.png)

![输入链接说明](https://bbs.django-vue-admin.com/uploads/20250321/c43aa51278cbc478287c718d22397479.png)


![输入链接说明](https://bbs.django-vue-admin.com/uploads/20250321/9732a5cca9c1166d1a65c35e313ab90d.png)


![输入链接说明](https://bbs.django-vue-admin.com/uploads/20250321/3ca9dd0801ce76d21435abcc8a3d505a.png)

![输入链接说明](https://bbs.django-vue-admin.com/uploads/20250321/a87a8d2329ef66880af5b0f16c5ff823.png)



