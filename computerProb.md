#### 搜狗输入法 适应日式键盘
https://notes.mengxin.science/2018/05/22/windows-sougou-keyboard-layout-by-regedit/
- KDJPN.DLL is japanese

#### bind ssh with github
```sh
$ ssh-keygen -t rsa -C "youremail@gmail.com"

// 1. select rsa save directory
// 2. enter password
// 3. go to github setting page
// 4. select add new ssh key, and paste the rsa.pub content to it -.-
```

#### connect ssh with github fail on windows
1. 添加rsa.pub to gihub
2. git-add id.rsa winsows显示could not open a connection to your authentication agent
3. windows要求先打开ssh客户端？ eval 'ssh-agent -s' 再ssh-add
4. ssh-add后显示id.rsa权限太open 不可以添加
5. chmod 0600 ~/.ssh/id.rsa 改权限 结果windows bash上更改无效？？？
6. stackoverflow上说要umount /mnt/c 结果也是一直busy没法umount 全局终

- 直接windows文件系统改权限呢？---没改明白
