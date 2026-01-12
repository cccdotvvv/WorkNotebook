obsidian 可以使用`control + P`来打开命令行，`git`插件具有大部分可用的操作。

# 1.  windows端

先使用 git bash 将远端的仓库拉取到本地，然后使用 obsidian 打开目标文件夹然后正常使用 git 插件进行操作即可。

# 2. ios端

1. ios 端需要先在 obsidian 上面建立一个本地的 vault 然后在文件 app 中才会出现 obsidian 的文件夹。
2. 下载 ish shell，参考[[ish shell配置]]进行相关配置，然后 cd 到 obsidian 的文件夹中拉取目标仓库。
3. 回到 obsidian 正常使用 git 插件同步笔记即可，第一次同步笔记的时候需要输入 username 和 密码，按正常流程进行操作即可。**注意：有一些网上的教程提到需要在 ish shell 中配置 git 的账户，但实际上在 ish shell 中配置完成之后不会在 obsidian 中生效，仍然会再次配置一次。**
4. 需要注意的是 git 要求输入的密码不是登陆密码，需要在“点击右上角头像 ->  Settings  -> 左侧边栏的  Developer settings  ->  Personal access tokens  ->  Tokens (classic) 。”中进行获取。
