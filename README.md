zabbix 企业微信报警.

调用企业微信API接口实现微信报警.

#Usage:
```
    Install:
        pip install zabbix-weixin-alert
        pip show zabbix-weixin-alert
```
[root@zabbix ~]# pip show zabbix-weixin-alert
DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 won't be maintained after that date. A future version of pip will drop support for Python 2.7.
Name: zabbix-weixin-alert
Version: 2019.2.27.1
Summary: zabbix qiye weixin alert
Home-page: https://github.com/talenhao/zabbix-weixin-alert
Author: Tianfei Hao
Author-email: talenhao@gmail.com
License: BSD License
Location: /usr/lib/python2.7/site-packages
Requires: requests
Required-by: 
```         
        In location path,copy /usr/lib/python2.7/site-packages/wxapi/zabbix-wx-alert.pyc to you zabbix-server alertscriptpath.

```
[root@zabbix ~ ]# cp /usr/lib/python2.7/site-packages/wxapi/zabbix-wx-alert.pyc /usr/lib/zabbix/alertscripts/ && chmod +x /usr/lib/zabbix/alertscripts/zabbix-wx-alert.pyc
```

    Add zabbix media with 6 Script parameters
        {ALERT.SENDTO}
        {ALERT.SUBJECT}
        {ALERT.MESSAGE}
        ww2489f02c7dxxxxxx # corpid
        et9Tkdp3ZkXAKpoxTdam6JRMgu2DRePLWmqB3xxxxxx # corp_secret
        1000002 # agentid
    add new media to users.

