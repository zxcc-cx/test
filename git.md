# Git

## 认知

### Repository

仓库：存放个人代码

* 多个仓库为`Repositories`

### star

收藏项目，便查看

### Fork

复制克隆项目：一个人的项目被另一个人拿去用作为自己的项目

### Pull Request

改进并向源码作者提供改进意见，源码拥有者同意即源码就会有改进内容

### watch

类似点击关注，会第一时间收到关注的更新提醒

### Issue

争论点：发现bug，提出Issue，由源码拥有者改进并close



### 页面

1. GitHub主页
2. 仓库主页
3. 个人主页

### Git工作区域

1. `Git request（Git仓库）`
2. `暂存区`
3. `工作区(Working Directory)`



## 命令

### Git`初始化`、`创建`、`操作`

> <big style="color:blue;font-weight:900;">初始化配置</big>
>
> ```
> $git config --global user.name '账户名'
> $git config --global user.name '邮箱号'
> ```
>
> 

> <big style="color:blue;font-weight:900;">初始化文件夹</big>
>
> ```
> $git init
> ```
>
> 注意：会生成`.git`的文件



> <big style="color:blue;font-weight:900;">本地仓库操作</big>
>
> + 查看文件状况
>
> ```
> $git status
> ```
>
> 
>
> + 提交至<a href="#">暂存区</a>
>
> ```
> //新增或修改时：
> $git add （文件名及路径）
> 
> //删除文件时：
> $git rm （文件名及路径）
> ```
>
> 
>
> + 提交到<a href="#">本地仓库</a>
>
> ```
> $git commit -m '提交描述'
> ```
>
> 
>
> + 提交到<a href="#">远程仓库</a>
>
> ```
> $git push
> ```
>
> 
>
> ##### 需要的`额外`命令
>
> > 当前文件夹下，创建新文件夹：
> >
> > ```
> > mkdir 文件夹名
> > ```
> >
> > 创建文件：
> >
> > ```
> > touch  文件名.格式
> > ```
> >
> > 查询当前文件所在路径：
> >
> > ```
> > pwd
> > ```
> >
> > 当前文件夹下，删除文件：
> >
> > ```
> > rm 文件名.格式
> > //或
> > rm -rf 文件名.格式
> > ```
> >



> <big style="color:blue;font-weight:900;">版本历史操作</big>
>
> + 查询
>
> ```
> //查询版本历史
> $git log
> 
> //推荐使用查询历史命令
> $git reflog
> $git log --oneline
> $git log --pretty=oneline
> ```
>
> + 回退历史版本
>
> ```
> //本地仓库版本前进后退，也会重置工作区和暂存区
> $git reset --hard  [索引值]	//索引值也可以是局部索引值
> 
> //只能后退，不能前进
> $git reset --hard HEAD^	//有几个^回退几个版本
> $git reset --hard HEAD~n	//回退n个版本
> 
> //可前进后退
> $git reset --soft	//仅在本地库移动HEAD指针，暂存区和工作区不变，
> $git reset --mixed	//只工作在暂存区和本地仓路
> 
> ```
>
> + 比较文件差异
>
> ```
> $git diff [文件名]	//工作区的新文件与暂存区的同名文件比较
> $git diff [本地库历史文件] [文件名]	//工作区的新文件与仓库历史版本同名文件比较
> ```
>
> \+



### `分支操作`

> <big style="color:blue;font-weight:900;">查看分支</big>
>
> ```
> $git branch -v	//查看所有的分支
> ```
>
> <big style="color:blue;font-weight:900;">创建分支</big>
>
> ```
> $git branch 分支名
> ```
>
> <big style="color:blue;font-weight:900;">切换分支</big>
>
> ```
> $git checkout 分支名
> ```
>
> <big style="color:blue;font-weight:900;">合并分支</big>
>
> *`注意`*：合并到目标上之前需在目标上操作（即切换至目标上）
>
> ```
> ......(目标)
> $git merge 分支名
> ```
>
> + 当分支合并有冲突时，需要在目标上(一般是master)协商并修改冲突部分



