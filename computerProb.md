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
- [solve] 改用git bash 解决了 windows的linux还是搞不懂

#### add local project to remote empty github repository
1. git add remote "remote repository name"
2. git remote -v  // verify the remote repository url
3. git push origin master

#### raspberryPI
##### 没有显示器，rasPi连入了无线网但是不知道IP
- 苹果的话 arp -a 可以查找同网段的机器，用了不好使，可能用的不对.
- ipscan22 windows工具可以很轻松的找到同网段的机器。T.T 困扰我这么长时间的问题
- [经验] 有问题先看一下有没有解决的软件工具，不一定非要是命令，尤其是在windows下命令行那么垃圾。