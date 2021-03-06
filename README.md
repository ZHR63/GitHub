# GItHub知识总结

我们一直用GitHub作为免费的远程仓库，如果是个人的开源项目，放到GitHub上是完全没有问题的。其实GitHub还是一个开源协作社区，通过GitHub，既可以让别人参与你的开源项目，也可以参与别人的开源项目。



### 在Windows上安装Git

从Git官网直接[下载安装程序](https://git-scm.com/downloads)

### git首次配置
    git config --global user.name 'ZHR63'
    git config --global user.email '634480610@qq.com'


### 本地与远程仓库的连接
    ssh-keygen -t rsa -C "634480610@qq.com"
    一直回车





* ### 文件修改后再次提交到远程仓库

-       git add .

-       git commit -m "内容"

-       git push origin master
        

* ### 远程仓库版本回退

-       1. 查看历史版本

        git log --pretty=oneline       
                
-       2. 回退到上一个版本

        git reset --hard HEAD^

-       3. 强制推送到远程仓库

        git push -f origin master
        

* ### 分支操作

-       创建分支

            git branch 名称

-       切换分支

            git checkout 分支名称

-       查看各个分支当前指向的对象

            git log --oneline --decorate

-       推送分支

            git push origin 分支名称
	
-       查看本地分支

            git branch

-       查看所有远程分支

            git branch -a

-       删除本地分支

            git branch -D 分支名称


* ### 拉取远程分支到本地

        1. git init
		
	    2. git remote add origin 远程仓库链接
		
 	    3. git fetch origin 远程仓库分支名称
		
   	    4. git pull origin 远程分支名称


* ### 内容修改完成后，提交到远程仓库

        1.切换到分支

	        git checkout 分支名称
			
	    2.git add .
		
	    3.git commit -m '修改内容'
		
	    4.提交到远程仓库

	        git push origin 分支名称
	    

	

* ### 远程分支合并

-      git clone 远程项目链接

-      在本地新建一个与远程的分支名称相同的分支名称

            git checkout -b 分支名称

-      远程分支代码pull到本地

            git pull origin 分支名称
    
-      如何有冲突的代码
        
            用 git status 查看冲突文件

            修改冲突代码后

            git add .

            git commit -m '输入内容'

-      git checkout  master

-      git merge 分支名称

-      git push origin master



* ### 多人协作开发

-      在项目的settings > Collaborators > Add collaborator 填写另一个开发者名称(对方的地址名称)，然后GigHub会发邮件等对方确认

  ![one](images/1.png)

-      协同者拉去源码到本地

            gig clone 远程仓库

-      协同者创建自己的分支

            git branch 分支名称

-      切换分支

            git checkout 分支名称
    
-      推送分支

            git push origin 分支名称
    
-      当协同者修改完成后

            git checkout 分支名称

            git add .

            git commit -m '修改内容'

            git push origin 分支名称


* ### GitHub上的README.md应该怎么写

    http://mahua.jser.me/ 个人开发的，免费使用，非常赞！

    http://maxiang.info/  已经发布的产品，可以免费在线编辑