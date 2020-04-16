# dd-moeclub
backup for dd script at moeclub.org

# DD步骤

## 下载脚本
```
wget 'https://raw.githubusercontent.com/ss-daily-backup/dd-moeclub/master/InstallNET.sh' && chmod a+x InstallNET.sh

yum install ca-certificates wget -y
apt-get install ca-certificates wget -y
wget 'https://raw.githubusercontent.com/ss-daily-backup/dd-moeclub/master/InstallNET-check-cert.sh' && chmod a+x InstallNET-check-cert.sh
```

## 如果服务商指定了DNS，需要先修改DNS，否则在网络下载时会出现 bad mirror 错误

将 8.8.8.8 替换为服务商提供的DNS，如 127.0.0.53 / 192.168.53.53
```
sed -i "s/8\.8\.8\.8/127\.0\.0\.53/g" InstallNET-check-cert.sh
sed -i "s/8\.8\.8\.8/192\.168\.53\.53/g" InstallNET-check-cert.sh
```

## 运行脚本
```
bash InstallNET.sh -d 9 -v 64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/'
bash InstallNET-check-cert.sh -d 9 -v 64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/'
bash InstallNET-check-cert.sh -d 9 -v 64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/' --password 'Password'
```
