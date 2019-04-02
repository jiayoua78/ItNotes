## Centos yum 安装Chrome

1. make yum resouce:into the folder `/etc/yum.repos.d/` then add a file `google-chrome.repo`

   edit the file `vim google-chrome.repo`  

```bash
[google-chrome]
name=google-chrome
baseurl=http://dl.google.com/linux/chrome/rpm/stable/$basearch
enabled=1
gpgcheck=1
gpgkey=https://dl-ssl.google.com/linux/linux_signing_key.pub
```

2. install

```bash
   yum -y install google-chrome-stable --nogpgcheck
```

   

