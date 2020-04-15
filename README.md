# dd-moeclub
backup for dd script at moeclub.org

```
wget 'https://raw.githubusercontent.com/ss-daily-backup/dd-moeclub/master/InstallNET.sh' && chmod a+x InstallNET.sh
wget 'https://raw.githubusercontent.com/ss-daily-backup/dd-moeclub/master/InstallNET-check-cert.sh' && chmod a+x InstallNET-check-cert.sh
```

```
bash InstallNET.sh -d 9 -v 64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/'
bash InstallNET-check-cert.sh -d 9 -v 64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/'
```
