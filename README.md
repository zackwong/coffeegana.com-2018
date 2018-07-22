coffeegana.com-2018
=============

咖纳贸易官网2018年版


域名绑定、301转向及nginx配置
-----

新建配置文件: ``sudo nano /etc/nginx/sites-available/coffeegana.com``

编辑配置文件及保存: 

    server {
        server_name coffeegana.com;
        return 301 http://www.coffeegana.com$request_uri;
    }
    server {
        server_name www.coffeegana.com;
        index index.html;
        root /srv/coffeegana.com-2018/_site;
        error_page 404 /Error.html;
    }

建立链接: ``sudo ln -s /etc/nginx/sites-available/coffeegana.com /etc/nginx/sites-enabled/``

重启nginx: ``sudo service nginx restart``


下载及生成网站
-----

1. 下载网站源码: ``git clone git://github.com/zackwong/coffeegana.com-2018.git``

2. 进入源码根目录: ``cd coffeegana.com-2018``

3. 生成网站: ``jekyll build``


开发者
---------

* Zack Wong &lt;hzzzoo@126.com&gt;

