使用方法：

使用root用户（可不加sudo）或者普通用户运行以下命令：

sudo yum install wget -y

sudo wget --no-check-certificate https://github.com/youchanlee/ssr/blob/master/ssr.sh

sudo chmod +x ssr.sh

sudo ./ssr.sh 2>&1 | tee ssr.log

安装完成后，脚本提示如下：


Congratulations, ShadowsocksR server install completed!

Your Server IP        :your_server_ip

Your Server Port      :your_server_port

Your Password         :your_password

Your Protocol         :your_protocol

Your obfs             :your_obfs

Your Encryption Method:your_encryption_method


Welcome to visit:https://github.com/youchanlee/ssr

Enjoy it!

卸载方法：

使用 root 用户登录，运行以下命令：


./shadowsocksR.sh uninstall

安装完成后即已后台启动 ShadowsocksR ，运行：


/etc/init.d/shadowsocks status

可以查看 ShadowsocksR 进程是否已经启动。

本脚本安装完成后，已将 ShadowsocksR 自动加入开机自启动。


使用命令：

启动：/etc/init.d/shadowsocks start

停止：/etc/init.d/shadowsocks stop

重启：/etc/init.d/shadowsocks restart

状态：/etc/init.d/shadowsocks status


配置文件路径：/etc/shadowsocks.json

日志文件路径：/var/log/shadowsocks.log

代码安装目录：/usr/local/shadowsocks


多用户配置示例：


{
"server":"0.0.0.0",

"server_ipv6": "[::]",

"local_address":"127.0.0.1",

"local_port":1080,

"port_password":{

    "8989":"password1",
    
    "8990":"password2",
    
    "8991":"password3"
    
},

"timeout":300,

"method":"aes-256-cfb",

"protocol": "origin",

"protocol_param": "",

"obfs": "plain",

"obfs_param": "",

"redirect": "",

"dns_ipv6": false,

"fast_open": false,

"workers": 1

}

-备份用途-
