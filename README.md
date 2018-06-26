知识工程作业说明：
小组成员：
杨帆（报告书写），焦超（网页交互界面设计），胡强强（sparql查询语句设计编写），龚凌云（图片爬虫代码编写）
使用步骤：
1、（1）Windows系统，有mysql环境（用来存储搜索内容）及python、
（2）django，selenium，SPARQLWrapper，（通过conda install或者pip install ）
2、将压缩包与chromedriver.exe下载下来，并将chromedriver.exe放到python的Scripts中
3、用mysql建立knowe数据库（create database knowe）
4、将解压后的文件app中的migrations中的0001_initial.py删除
5、在manage.py所在目录打开cmd，运行python manage.py makemigrations，然后运行python manage.py migrate（mysql处于开启状态）
6、运行python manage.py runserver
7、在浏览器输入http://127.0.0.1:8000，即可打开搜索界面
8、存在的不足：
（1）爬虫爬取图片会跳出谷歌浏览器页面（稍后关闭），所以整个查询时间较长
（2）若是爬取不到的图片，都使用了自定义的网络图片
（3）由于搜索语句存在很多限制，当输入搜索不到时，界面一般无反应，后台有搜索失败的错误
