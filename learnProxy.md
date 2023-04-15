linux 使用代理

```shell

#配置代理
echo 'export http_proxy="192.168.31.109:7890"' >> /etc/profile
echo 'export https_proxy="192.168.31.109:7890"' >> /etc/profile

#验证
wget www.google.com

#取消代理
unset http_proxy
unset https_proxy
```

Debian 
https://blog.csdn.net/weixin_44071721/article/details/127162380

# 设置代理；
echo 'export https_proxy="http://192.168.31.109:7890"' >> ~/.bashrc
echo 'export http_proxy=$https_proxy' >> ~/.bashrc
echo 'export ftp_proxy=$https_proxy' >> ~/.bashrc
echo 'export proxy=$https_proxy' >> ~/.bashrc
echo 'export HTTPS_PROXY=$https_proxy' >> ~/.bashrc
echo 'export HTTP_PROXY=$https_proxy' >> ~/.bashrc
echo 'export FTP_PROXY=$https_proxy' >> ~/.bashrc
echo 'export PROXY=$https_proxy' >> ~/.bashrc
# 取消代理；
vim ~/.bashrc # 编辑.bashrc文件删除或注释代理设置；

# 设置代理；
echo 'https_proxy=http://192.168.31.109:7890' | tee -a /etc/wgetrc
echo 'http_proxy=http://192.168.31.109:7890' | tee -a /etc/wgetrc
echo 'ftp_proxy=http://192.168.31.109:7890' | tee -a /etc/wgetrc
echo '#check_certificate = off' >> ~/.wgetrc
# 取消代理；
vim /etc/wgetrc # 编辑wgerrc文件删除或注释代理设置；
