### arch linux -- git flow

#### window

```
$ wget -q -O - --no-check-certificate https://github.com/nvie/gitflow/raw/develop/contrib/gitflow-installer.sh | bash
```
这里你需要wget 和 util-linux

#### Ubuntu

```
apt-get install git-flow
```

#### other linux
```
$ curl -OL https://raw.github.com/nvie/gitflow/develop/contrib/gitflow-installer.sh
$ chmod +x gitflow-installer.sh
$ sudo ./gitflow-installer.sh
```

### git flow 使用

#### git flow 初始化
```
git flow init
```

#### 开发新特性
```
git flow feature start MYFEATURE
```
它会创建一个分支feature/demo，并切换到该分支。
当功能完成时
```
git flow feature finish demo
```
它会有feature/demo分支合并到develop分支，然后切换回develop分支，并删除feature/demo分支。

```
git flow release start v0.7.0
```
它会创建一个release/v0.7.0分支，并切换到该分支。
然后在这里进行测试。如果测试没问题，则执行以下命令：
```
git flow release finish v0.7.0
```
它会将release/v0.7.0分支的内容合并到master分支和develop分支，并且打上tag v0.7.0，然后删除release/v0.7.0分支。

#### 修复bug
```
git flow hotfix start 3

```
它会创建一个基于master的分支hotfix/3，并切换到当前分支。
当修复完成后，可以执行以下命令：
```
git flow notfix finish 3
```
[参考文章1](http://www.bkjia.com/Javabc/1156134.html)
[参考文章2](https://github.com/nvie/gitflow/wiki/Linux)
[参考文章3](https://juejin.im/entry/56f50894da2f60004c4ee203)
[git flow wiki](https://github.com/nvie/gitflow/wiki/Windows)
