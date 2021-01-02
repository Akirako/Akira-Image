# Github + PicGo 共建的图床服务

相关项目：
* [jsDelivr - CDN](https://www.jsdelivr.com/)
* [PicGo - 一个用于快速上传图片并获取图片 URL 连接的工具](https://github.com/Molunerfinn/PicGo)

### 如何使用？

1. 下载安装 [PicGo](https://github.com/Molunerfinn/PicGo/releases)。
2. 在 [GitHub](https://github.com/new) 上创建新的仓库。
3. 根据如下步骤，生成并保存 GitHub 的个人访问令牌（Token）。
4. 配置 PicGo - 图床设置。

### 生成 GitHub Token

在 GitHub 页面右上角点击个人头像，进入 “Settings”。

![进入 GitHub Settings](https://cdn.jsdelivr.net/gh/Akirako/Akira-Image/photo/20210102142114.jpg
)

接着点击进入左边导航栏中的 “Developer settings”，找到 “Personal access tokens”，在右上位置处点击 “Generate new token” 生成新令牌。

![点击 “Generate new token” 生成新令牌](https://cdn.jsdelivr.net/gh/Akirako/Akira-Image/photo/20210102142923.jpg
)

输入名称，勾选 “repo”，其他的不用勾选。

![](https://cdn.jsdelivr.net/gh/Akirako/Akira-Image/photo/20210102144459.png
)

接着将进入如下页面，方框标记中的就是需要的 Token，点击它旁边的按钮可以复制。

![](https://cdn.jsdelivr.net/gh/Akirako/Akira-Image/photo/20210102143811.png
)

保存好生成的个人访问令牌（Personal access tokens），因为该页面只会显示一次。

### 配置 PicGo 图床设置

在 PicGo 页面中点击 “图床设置”，找到 “Github图床”，填写配置。

![](https://cdn.jsdelivr.net/gh/Akirako/Akira-Image/photo/20210102144847.jpg
)

#### 设定仓库名称：

仓库名称是你的 GitHub 用户名加上 `/` 你的仓库名。或者是你在浏览器中访问到你仓库的链接去掉前面的 `https://github.com/` 后的剩余部分。

![](https://cdn.jsdelivr.net/gh/Akirako/Akira-Image/photo/20210102145659.jpg
)

#### 设定分支：

填 “master”。

#### 设定Token：

复制刚才 GitHub 生成的 “Token”

#### 指定存储路径：

就是在该仓库下哪个文件夹用来存放图片，比如填写 `photo/` 就会在该仓库下名为 “photo” 的文件中上传图片，如果没有，则会创建一个名为 “photo” 的文件夹。**注意**，后面要有 `/`。

#### 设定自定义域名：

这里可以利用 jsDelivr 为访问 GitHub 提供加速，以便在国内访问你博客中的图片时能快速的加载出来。

设置如下：

`https://cdn.jsdelivr.net/gh/用户名/仓库名`

比如：

`https://cdn.jsdelivr.net/gh/Akirako/Akira-Image`

