# BIT-Srun-Login-Public
 
## Overview
北京理工大学（Beijing Institute of Technology）命令行登录校园网脚本。
为了帮助大家在疫情期间更好的利用校园网进行“炼丹”，该脚本通过requests帮助大家模拟校园网登录，可以在没有图形界面的情况下登录校园网。

## 前提

通过如下方法安装：
```bash
pip install bitsrunlogin
```
仅在python3下进行了测试，不保证其他环境下的有效性。

## 单次登录

进入python下的命令模式，
```python3
from bitsrunlogin.LoginManager import LoginManager
lm = LoginManager()
lm.login(
    username = "Your srun account",
    password = "Your password"
)
```

或者可以通过demo.py直接运行;  
username和password对应校园网账户的用户名与密码，填写后运行即可实现外网连接。
```bash
python3 demo.py
```

## 保持在线
online.py脚本可以帮助用户保持在线，每5min检查网络的在线状态，如果存在掉线情况，自动重新登录。
```bash
python3 onine.py
```

也可以通过`nohup`命令在后台保持运行，或者添加到开机自动启动程序中。
```bash
nohup python3 always_online.py &
```
## Acknowledge
改脚本引用了 [coffeehat](https://github.com/coffeehat/BIT-srun-login-script)的工作。
