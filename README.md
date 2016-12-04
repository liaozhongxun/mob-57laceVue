==> git命令中一般 - 跟简称 -- 跟全称 （ 如: -h/--help）

==> git init  //创建本地git仓库

==> git config -h //帮助

==> git config --list  //查看git所有配置

    git 配置分为三部分

        1、本地配置位于本地仓库的隐藏文件夹.git/config 文件  默认以core开头

           git config --local --list (只 本地配置)

        2、全局配置位于用户的根目录下 .gitconfig  //需要进行过全局配置才会有该文件

           git config --global --list (只 全局配置)

        3、系统配置位于git的安装目录下

           git config --system --list (只 系统配置)

        (优先级依次降低 如果三个配置文件中都有同样的配置优先以本地为准)

==>  git config --[local/global/system] obj.键 + 空格 + 值 //修改、添加配置

==>  git config --[local/global/system] --unset obj.键  //删除配置

==================git分区

==> 工作区 (.git 所在的工作目录)

==> 暂存区

==> 仓库 （.git 这个目录就是仓库）


==> git status 查看文件状态

    刚新建的文件/修改 --> 未跟踪的文件（红色不会被提交）

    git add 文件名/夹  --> 成为跟踪文件 (绿色)
    git rm --cached 文件名 --> 取消跟踪状态

    git commit -m "提交说明" || 

    git commit 回车(进入编辑器) --> i(进入编辑模式) --> esc (退出编辑模式) --> :wq(保存并退出)



==> git checkout 检出文件(当一个文件改错了 想从历史中拿一个版本来替换是做的)

    git checkout  通过commit id 指定哪个版本(没指定的话就用最近一次提交的版本) 文件名




==> 忽略文件 （成功之后查看状态时就不会显示它了）

    1、工作区根目录下 创建文件 .gitignore 文件

    2、规定忽略规则(在文件里写入文件/文件夹名就好 可以是路径（更多...）)

    3、该文件可存在于个个目录


==> git log 查看日志

   1、commit id  重要


==================远程仓库

==> github

==> 开源中国

    链接 : git remote add origin https://git.oschina.net/liaozhongxun/mob-57laceVueChina.git  
                          git@git.oschina.net:liaozhongxun/mob-57laceVueChinaRecommend_gray-.git

    推送 : git push -u origin master

    本地仓库与远程仓库名必须相同 


==> 生产本机的ssh  

    1、git下输入  ssh-keygen  连续回车生成公私钥（公私钥与本台计算机有关）

    2、公私钥匙用户家目录下的 .ssh 文件夹中

       私钥 : id_rsa 

       公钥 : id_rsa.pub

    3、复制公钥的内容到远程仓库(GitHub 或 开源中国等）

       添加成功后本台计算机就能和远程仓库进行交换了


==> git命令中一般 - 跟简称 -- 跟全称 （ 如: -h/--help）

==> git init  //创建本地git仓库

==> git config -h //帮助

==> git config --list  //查看git所有配置

    git 配置分为三部分

        1、本地配置位于本地仓库的隐藏文件夹.git/config 文件  默认以core开头

           git config --local --list (只 本地配置)

        2、全局配置位于用户的根目录下 .gitconfig  //需要进行过全局配置才会有该文件

           git config --global --list (只 全局配置)

        3、系统配置位于git的安装目录下

           git config --system --list (只 系统配置)

        (优先级依次降低 如果三个配置文件中都有同样的配置优先以本地为准)

==>  git config --[local/global/system] obj.键 + 空格 + 值 //修改、添加配置

==>  git config --[local/global/system] --unset obj.键  //删除配置

==================git分区

==> 工作区 (.git 所在的工作目录)

==> 暂存区

==> 仓库 （.git 这个目录就是仓库）


==> git status 查看文件状态

    刚新建的文件/修改 --> 未跟踪的文件（红色不会被提交）

    git add 文件名/夹  --> 成为跟踪文件 (绿色)
    git rm --cached 文件名 --> 取消跟踪状态

    git commit -m "提交说明" || 

    git commit 回车(进入编辑器) --> i(进入编辑模式) --> esc (退出编辑模式) --> :wq(保存并退出)

    链接 : git remote add origin  http.. || ssh

    推送 : git push -u origin master(分支)  (第二次就直接push就行了)

==> git pull 拉取远程仓库内容到本地(更新)

==> git branch 分支名 //新建分支

    git branch 分支名 'commit id' //基于某一次提交的分支

    git branch  //查看分支 前面有 * 的就是当前指向的分支(head指向的分支)

    git checkout 分支名 //切换到该分支(会检出该分支最后一次提交的代码到工作区)


==> git clone http.. || ssh  克隆远程仓库

==> git checkout 检出文件(当一个文件改错了 想从历史中拿一个版本来替换是做的)

    git checkout  通过commit id 指定哪个版本(没指定的话就用最近一次提交的版本) 文件名


==> git status //贮藏工作区(保存当前修改又不想提交的文件 之后)

    git status show 查看贮藏内容

    git status pop 取出贮藏内容


==> 忽略文件 （成功之后查看状态时就不会显示它了）

    1、工作区根目录下 创建文件 .gitignore 文件

    2、规定忽略规则(在文件里写入文件/文件夹名就好 可以是路径（更多...）)

    3、该文件可存在于个个目录


==> git log 查看日志

   1、commit id  重要


==================远程仓库

==> github

==> 开源中国

    本地仓库与远程仓库名必须相同 

==> 生产本机的ssh  

    1、git下输入  ssh-keygen  连续回车生成公私钥（公私钥与本台计算机有关）

    2、公私钥匙用户家目录下的 .ssh 文件夹中

       私钥 : id_rsa 

       公钥 : id_rsa.pub

    3、复制公钥的内容到远程仓库(GitHub 或 开源中国等）

       添加成功后本台计算机就能和远程仓库进行交换了


