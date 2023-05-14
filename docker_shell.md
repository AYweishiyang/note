docker脚本整理

```shell
netdata

docker run -d --name=netdata \
-p 19999:19999 \
-v netdataconfig:/etc/netdata \
-v netdatalib:/var/lib/netdata \
-v netdatacache:/var/cache/netdata \
-v /etc/passwd:/host/etc/passwd:ro \
-v /etc/group:/host/etc/group:ro \
-v /proc:/host/proc:ro \
-v /sys:/host/sys:ro \
-v /etc/os-release:/host/etc/os-release:ro \
--restart unless-stopped \
--cap-add SYS_PTRACE \
--security-opt apparmor=unconfined \
netdata/netdata

firefox
docker run -d --name=firefox -p 5800:5800 -p 5900:5900 --shm-size 2g -e DISPLAY_WIDTH=1366 -e DISPLAY_HEIGHT=768 swr.cn-north-1.myhuaweicloud.com/iivey/firefox:v1.1


```

