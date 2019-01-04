# pierced
钉钉内网穿透

ding -config=ding.cfg -subdomain=abcde 8080
访问http://abcde.vaiwan.com/xxxxx都会映射到 http://127.0.0.1:8080/xxxxx

TCP 穿透需要在数据库里面执行：
GRANT ALL PRIVILEGES ON *.* TO root@'%' IDENTIFIED BY '123456';
FLUSH PRIVILEGES;
数据库连接命令：
mysql -h vaiwan.com -u root -p -P 1234 //端口号地址
