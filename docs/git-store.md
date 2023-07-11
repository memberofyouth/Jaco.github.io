```
ssh设置

删除.ssh下所有文件

设置用户名、邮箱

git config --global user.name 'ringluck'

git config --global user.email 'mrzlive@163.com'

git config --list

生成公私钥

ssh-keygen -t rsa -C "mrzlive@163.com"


```







```
cd ~

touch .git-credentials

vim .git-credentials

http://username:password@gitlab.ziggurat.cn/taizhou/taizhou.git

git config --global credential.helper store


```







git remote add origin ***.git
git push -u origin master









**1.显示所有的tag**

```text
git tag
```

**2.查看某个版本系统的tag**

```text
git tag -l   ' v1.0.*'
```

**3. 创建标签**

```text
第一种: git tag -a v1.0.0 -m '内容'
第二种: git tag v1.0.0
```

**4.查看标签的详情**

```text
git show v1.0.0
```

得到以下输出：

```text
commit a83516d0fb5da5fd5ad749733a160219b5a5ceac (tag: v1.0.0) 
Author: Alfred Liu <joemale@163.com>
```

**5.推送标签**

```text
git push origin v1.0.0
```

**6.删除标签**

- 删除本地标签

```text
git tag -d v1.0.0
```

- 删除远程标签

```text
git push origin :refs/tags/pre-v1.2.0
```

- **完整的打tag**

```text
git add *
git commit -m 'v1.0.0'
git tag v1.0.0
git push
git push origin v1.0.0
```

### 7.删除远程分支

```
删除 origin/test 分支：

git push origin -d test
```

