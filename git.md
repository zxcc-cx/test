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
> git config --global user.name '账户名'
> git config --global user.name '邮箱号'
> ```
>
> 

> <big style="color:blue;font-weight:900;">初始化文件夹</big>
>
> ```
> git init
> ```
>
> 注意：会生成`.git`的文件



> <big style="color:blue;font-weight:900;">操作</big>
>
> 1. 查看文件状况
>
>    ```
>    git status
>    ```
>
> 
>
> 2. 提交至<a href = “#">暂存区</a>
>
>    ```
>    //新增或修改时：
>    git add （文件名及路径）
>    
>    删除文件时：
>    git rm （文件名及路径）
>    ```
>
> 
>
> 3. 提交到<a href="#">本地仓库</a>
>
>    ```
>    git commit -m '提交描述'
>    ```
>
> 
>
> 4. 提交到<a href="#">远程仓库</a>
>
>    ```
>    git push
>    ```
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
> > 
