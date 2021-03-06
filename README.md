# DecryptLogin
```
APIs for loginning some websites using <requests>.
You can star this repository to keep track of the project if it's helpful for you, thank you for your support.
```

# Documents
#### In Chinese
https://httpsgithubcomcharlespikachudecryptlogin.readthedocs.io/zh/latest/
#### In English
https://httpsgithubcomcharlespikachudecryptlogin.readthedocs.io/en/latest/

# Support List
|  Websites        | support PC API?    |  support mobile API?     |  in Chinese    |
|  :----:          | :----:             |  :----:                  |  :----:        |
|  weibo           | ✓                  |  ✓                       |  新浪微博      |
|  douban          | ✓                  |  ✗                       |  豆瓣          |
|  github          | ✓                  |  ✗                       |  Github        |
|  music163        | ✓                  |  ✗                       |  网易云音乐    |
|  zt12306         | ✓                  |  ✗                       |  中国铁路12306 |
|  QQZone          | ✗                  |  ✓                       |  QQ空间        |
|  QQQun           | ✗                  |  ✓                       |  QQ群          |
|  QQId			   | ✗                  |  ✓                       |  我的QQ中心    |
|  zhihu		   | ✓                  |  ✗                       |  知乎          |
|  bilibili		   | ✓                  |  ✓                       |  B站           |
|  toutiao		   | ✗                  |  ✓                       |  今日头条      |
|  taobao          | ✓                  |  ✗                       |  淘宝          |
|  jingdong        | ✓                  |  ✗                       |  京东          |
|  ifeng           | ✓                  |  ✗                       |  凤凰网        |
|  sohu            | ✓                  |  ✓                       |  搜狐          |
|  zgconline       | ✓                  |  ✗                       |  中关村在线    |
|  lagou           | ✓                  |  ✗                       |  拉勾网        |
|  twitter         | ✓                  |  ✗                       |  推特          |
|  Vultr           | ✓                  |  ✗                       |  Vultr         |

# Some Cases by Using DecryptLogin
|  Name                       |   Introduction                                                   |   code                                                                                                       |  in Chinese                     |
|  :----:                     |   :----:                                                         |   :----:                                                                                                     |  :----:                         |
|  weiboMonitor               |   [click](https://mp.weixin.qq.com/s/uOT1cGqXkOq-Hdc8TVnglg)     |   [click](https://github.com/CharlesPikachu/DecryptLogin/tree/master/examples/weiboMonitor)                  |  微博监控                       |
|  QQReport                   |	  [click](https://mp.weixin.qq.com/s/dsVtEp_TFeyeSAAUn1zFEw)     |	 [click](https://github.com/CharlesPikachu/DecryptLogin/tree/master/examples/QQReport)                      |  生成QQ个人专属报告             |
|  bilibiliDownloadUserVideos |   [click](https://mp.weixin.qq.com/s/GaVW4_nbAaO0QvphI7QgnA)     |   [click](https://github.com/CharlesPikachu/DecryptLogin/tree/master/examples/bilibiliDownloadUserVideos)    |  下载B站指定UP主的所有视频      |
|  NeteaseSongListDownloader  |   [click](https://mp.weixin.qq.com/s/_82U7luG6jmV-xb8-Qkiew)     |   [click](https://github.com/CharlesPikachu/DecryptLogin/tree/master/examples/NeteaseSongListDownloader)     |  网易云个人歌单下载器           |
|  NeteaseListenLeaderboard   |   [click](https://mp.weixin.qq.com/s/Wlf1a82oACc9N7zGezcy8Q)     |   [click](https://github.com/CharlesPikachu/DecryptLogin/tree/master/examples/NeteaseListenLeaderboard)      |  网易云个人听歌排行榜           |
|  userWeiboSpider            |   [click](https://mp.weixin.qq.com/s/-3BDTZAE1x7nfCLNq2mFBw)     |   [click](https://github.com/CharlesPikachu/DecryptLogin/tree/master/examples/userWeiboSpider)               |  下载指定微博用户的所有微博数据 |

# Install
#### Pip install
```
run "pip install DecryptLogin"
```
#### Source code install
```sh
(1) Offline
Step1: git clone https://github.com/CharlesPikachu/DecryptLogin.git
Step2: cd DecryptLogin -> run "python setup.py install"
(2) Online
run "pip install git+https://github.com/CharlesPikachu/DecryptLogin.git@master"
```

# Usage
#### Arguments
```
Specific Loginning Arguments:
--username: your username.
--password: your password.
--mode: pc/mobile.
--crackvcFunc: an user-defined function used to crack the verification code (usage: crackvcFunc(verification_code_path)).
--proxies: adopt specified proxies to login the website.
```
#### Quick Start
```python
from DecryptLogin import login
lg = login.Login()
infos_return, session = lg.douban(username[telephone], password, 'pc')
infos_return, session = lg.github(username[email], password, 'pc')
infos_return, session = lg.weibo(username[telephone], password, 'mobile')
infos_return, session = lg.music163(username[telephone/email], password, 'pc')
infos_return, session = lg.zt12306(username[telephone], password, 'pc')
infos_return, session = lg.QQZone('mobile')
infos_return, session = lg.QQQun('mobile')
infos_return, session = lg.QQId('mobile')
infos_return, session = lg.zhihu(username, password, 'pc')
infos_return, session = lg.bilibili(username, password, 'pc')
infos_return, session = lg.toutiao(username, password, 'mobile')
infos_return, session = lg.taobao('pc')
infos_return, session = lg.jingdong('pc')
infos_return, session = lg.ifeng(username, password, 'pc')
infos_return, session = lg.sohu(username, password, 'mobile')
infos_return, session = lg.zgconline(username, password, 'pc')
infos_return, session = lg.lagou(username, password, 'pc')
infos_return, session = lg.twitter(username, password, 'pc')
infos_return, session = lg.vultr(username, password, 'pc')
```
#### Detailed documentation
```
The detailed documentation for DecryptLogin is here:
https://httpsgithubcomcharlespikachudecryptlogin.readthedocs.io/zh/latest/ (In Chinese)
https://httpsgithubcomcharlespikachudecryptlogin.readthedocs.io/en/latest/ (In English)
```

# Thanks List
|  Author                                            |           Time            |   Contribution                                     |
|  :----:                                            |           :----:          |   :----:                                           |
|  @[skygongque](https://github.com/skygongque)      |           2020-02-13      |   add verification code processing in (weibo, pc)  |

# More
#### WeChat Official Accounts
*Charles_pikachu*  
![img](pikachu.jpg)