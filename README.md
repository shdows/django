# django教程

## django的安装
一般使用pip进行django安装，但是由于django包比较大，安装速度慢，需要替换为国内
的源。下面使用的是清华的源，更换pip得源得配置如下：
> linux中修改 ~/.pip/pip.conf (没有就创建一个)， 内容如下：     
[global]    
index-url = https://pypi.tuna.tsinghua.edu.cn/simple    
[install]   
trusted-host = https://pypi.tuna.tsinghua.edu.cn
>
> windows上的修改   
在user的用户下目录中创建一个pip目录，如：C:\Users\用户名xx\pip,
新建文件pip.ini，内容如下:
[global]    
index-url = https://pypi.tuna.tsinghua.edu.cn/simple    
[install]   
trusted-host = https://pypi.tuna.tsinghua.edu.cn

## 入门
> 详情见[入门](quick_start.md)