# 1. 自定义安装路径

使用指令
`powershell -ExecutionPolicy ByPass -c {$env:UV_INSTALL_DIR = "D:\Program Files\uv";irm https://astral.sh/uv/install.ps1 | iex}`
进行安装可以自定义安装路径，修改`$env:UV_INSTALL_DIR = "D:\Program Files\uv"`中的路劲即可。

# 2. 自定义python、缓存等保存位置

windows在系统的环境变量中添加环境变量即可，可以使用powertshell快捷添加相关的环境变量。

```powershell
[Environment]::SetEnvironmentVariable("UV_CACHE_DIR", "path\to\cache", "User")
[Environment]::SetEnvironmentVariable("UV_PYTHON_BIN_DIR", "path\to\install", "User")
[Environment]::SetEnvironmentVariable("UV_PYTHON_INSTALL_DIR", "path\to\python", "User")
[Environment]::SetEnvironmentVariable("UV_TOOL_BIN_DIR", "path\to\install", "User")
[Environment]::SetEnvironmentVariable("UV_TOOL_DIR", "path\to\tool", "User")
[Environment]::SetEnvironmentVariable("UV_DEFAULT_INDEX", "https://pypi.tuna.tsinghua.edu.cn/simple", "User")
```
这条指令除了更改python的安装位置之外还会更改pypi源为清华源，并且所有环境变量都是**用户**级别。