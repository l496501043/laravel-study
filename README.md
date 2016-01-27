##Mac os x安装laravel框架小结<br/>
#1.环境：
	国内local环境，mac＋apache＋php5.6.17
#2.准备：
	git clone https://github.com/laravel/laravel.git获取官方代码
#3.安装：
	程序下拷贝下来后准备composer安装（`sudo composer install`）  
结果国内镜像有问题还是怎么回事，总是失败，然后去我的香港vps上面把第二步和composer install走了一遍，把vendor目录拷贝下来放在laravel根目录  
如果没有进行`composer install`的话，会报这样的错误：  
Warning: require(/Users/liugx/work/laravel/bootstrap/../vendor/autoload.php): failed to open stream: No such file or directory in /Users/liugx/work/laravel/bootstrap/autoload.php on line 17   
#4.开始laravel：
	安装好后，想在/hello下输出个hello，world！，配置路由不输出，这是由于我的apache是新配置的。  
sudo vi /etc/apache2/httpd.conf  
查找到mod_rewrite.so ，将这行前面的注释符号＃去掉，然后找到httpd-vhost.conf中AllowOverride None改成AllowOverride All								
#5.可以愉快的玩耍了。
