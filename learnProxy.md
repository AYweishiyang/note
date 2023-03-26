#配置代理
echo 'export http_proxy="192.168.31.109:7890"' >> /etc/profile
echo 'export https_proxy="192.168.31.109:7890"' >> /etc/profile

#验证
wget www.google.com

#取消代理
unset http_proxy
unset https_proxy
