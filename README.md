# 企业微信工具

这是一个基于企业微信 API 开发的用于消息通知的 Python 库

## Guide

开始之前，请先跟随一下步骤创建一个企业微信应用

- [注册/登录企业微信管理后台](https://work.weixin.qq.com/)
- [创建/查看/管理应用](https://work.weixin.qq.com/wework_admin/frame#apps)
- [查看企业ID](https://work.weixin.qq.com/wework_admin/frame#profile)
- [查看企业微信成员信息](https://work.weixin.qq.com/wework_admin/frame#contacts)
- [添加插件以支持推送到个人微信](https://work.weixin.qq.com/wework_admin/frame#profile/wxPlugin)

## Installation

- 通过 `pip` 安装

```bash
pip install wechat_work
```

- 通过 `git` 和 `pip` 安装

```bash
pip install git+https://github.com/Micro-sheep/wechat_work.git
```

## Examples

```python
from wechat_work import WechatWork
corpid = '企业 ID'
appid = '企业应用 ID'
corpsecret = '企业应用 Secret'
users = ['企业微信的用户账号1', '企业微信的用户账号2']
w = WechatWork(corpid=corpid,
               appid=appid,
               corpsecret=corpsecret)
# 发送文本
w.send_text('Hello World!', users)
# 发送 Markdown
w.send_markdown('# Hello World', users)
# 发送图片
w.send_image('./hello.jpg', users)
# 发送文件
w.send_file('./hello.txt', users)

```
