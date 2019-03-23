                    # SSR

ShadowsocksR 一键管理脚本 [v2.0.38]
  ---- Toyo | doub.io/ss-jc42 ----

    1. 安装 ShadowsocksR
    2. 更新 ShadowsocksR
    3. 卸载 ShadowsocksR
    4. 安装 libsodium(chacha20)
------------------------------------
    5. 查看 账号信息
    6. 显示 连接信息
    7. 设置 用户配置
    8. 手动 修改配置
    9. 切换 端口模式
------------------------------------
  10. 启动 ShadowsocksR
  11. 停止 ShadowsocksR
  12. 重启 ShadowsocksR
 13. 查看 ShadowsocksR 日志
------------------------------------
  14. 其他功能
  15. 升级脚本

 当前状态: 未安装



SSR账号端口：4359

SSR 账号密码：@Bb018zck9920SS}2D

---

ShadowsocksR账号 配置信息：

 I  P       : 168.63.201.221
 端口       : 4359
 密码       : @Bb018zck9920SS}2D
 加密       : aes-256-cfb
 协议       : origin
 混淆       : plain
 设备数限制 : 10
 单线程限速 : 0 KB/S
 端口总限速 : 0 KB/S



 SS    [链接](ss://YWVzLTI1Ni1jZmI6QEJiMDE4emNrOTkyMFNTfTJEQDE2OC42My4yMDEuMjIxOjQzNTk)
 SS   [二维码](http://doub.pw/qr/qr.php?text=ss://YWVzLTI1Ni1jZmI6QEJiMDE4emNrOTkyMFNTfTJEQDE2OC42My4yMDEuMjIxOjQzNTk)
 SSR  [链接](ssr://MTY4LjYzLjIwMS4yMjE6NDM1OTpvcmlnaW46YWVzLTI1Ni1jZmI6cGxhaW46UUVKaU1ERTRlbU5yT1RreU1GTlRmVEpF) 
 SSR [二维码](http://doub.pw/qr/qr.php?text=ssr://MTY4LjYzLjIwMS4yMjE6NDM1OTpvcmlnaW46YWVzLTI1Ni1jZmI6cGxhaW46UUVKaU1ERTRlbU5yT1RreU1GTlRmVEpF)

  提示:
 在浏览器中，打开二维码链接，就可以看到二维码图片。
 协议和混淆后面的[ _compatible ]，指的是 兼容原版协议/混淆。

#### 脚本的一些常用命令

**启动 ShadowsocksR：**/etc/init.d/ssr start

**停止 ShadowsocksR：**/etc/init.d/ssr stop

**重启 ShadowsocksR：**/etc/init.d/ssr restart

**查看 ShadowsocksR状态：**/etc/init.d/ssr status

---

# Kcptun

- Port:4859

- key:Hnjks+=)}{plk23FRS

- crypt:

**服务器配置**

```json
{
"listen": ":4859",
"target": "127.0.0.1:4359",
"key": "Hnjks+=)}{plk23FRS",
"crypt": "aes",
"mode": "fast2",
"mtu": 1350,
"sndwnd": 128,
"rcvwnd": 1024,
"datashard": 70,
"parityshard": 3,
"dscp": 0,
"nocomp": false,
"acknodelay": false,
"nodelay": 0,
"interval": 40,
"resend": 0,
"nc": 0,
"sockbuf": 4194304,
"keepalive": 10
}
```

**重新配置：**./kcptun.sh reconfig

**卸载：**./kcptun.sh uninstall





### KCPTUN 官网

### [github地址](https://github.com/xtaci/kcptun)



