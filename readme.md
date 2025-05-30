
# 镜像地址

```json
docker login ccr.ccs.tencentyun.com --username=100015489703

密码 咨询田老师/飞书权限

docker pull ccr.ccs.tencentyun.com/xiaoyibao/dow-gewe-official-simplified-xyb:v5
```

## docker-compose.yml配置中，端口映射配置需要和公网开放的端口一致。家里我直接偷懒，用了9919端口，转发到本地MAC电脑IP的9919端口。    
```json
        ports:
      - "9919:9919"
```


# config.json配置中，必须是公网IP + 公网开放的端口才可以。
```json
    "gewechat_callback_url": "http://112.65.86.214:9919/v2/api/callback/collect"
```

重启后就可以启动了，扫码登录。

# 修改插件
```json
- plugins/hello中修改欢迎词
- plugins/lcard中修改和增加卡片
- 插件过多容易封号

```
