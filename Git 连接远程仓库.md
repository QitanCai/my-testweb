# Git 连接远程仓库

>   Git 并不像 SVN 那样有个中心服务器。
>
>   目前我们使用到的 Git 命令都是在本地执行，如果你想通过 Git 分享你的代码或者与其他开发人员合作。 你就需要将数据放到一台其他开发人员能够连接的服务器上。

## 连接远程仓库

>   由于你的本地 Git 仓库和 GitHub 仓库之间的传输是通过SSH加密的，所以我们需要配置验证信息：

#### 配置验证信息

使用以下命令生成 SSH Key：

`$ ssh-keygen -t rsa -C "youremail@example.com"`

之后一路回车

<img src="Git%20%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.assets/image-20210317143325930.png" alt="image-20210317143325930" style="zoom:80%;" />

回到 github 上，进入 Account => Settings（账户配置）：

<img src="Git%20%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.assets/image-20210317143410509.png" alt="image-20210317143410509" style="zoom: 50%;" />

左边选择 **SSH and GPG keys**，然后点击 **New SSH key** 按钮，title 设置标题，可以随便填，粘贴在你电脑上生成的 key。	

<img src="Git%20%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.assets/image-20210317145441807.png" alt="image-20210317145441807" style="zoom: 50%;" />

为了验证是否成功，输入以下命令：

![image-20210317145756717](Git%20%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.assets/image-20210317145756717.png)

以下命令说明我们已成功连上 Github。

## 提取远程仓库到本地仓库

0、添加远程仓库

`git remote add origin git@github.com:yourGithubId/repository`

1、从远程仓库下载新分支与数据

`git fetch`

2、从远端仓库提取数据并尝试合并到当前分支：

`git merge`