# Dukou每日签到+转换流量
__Forked from [dukou_checkin](https://github.com/lycstar/dukou_checkin)__

## 使用
使用 github action 每日定时功能

1. Fork 本项目

2. 添加 Secrets

   方法：Settings -> Secrets -> New repository secret

    - EMAIL_KEY (邮箱,必填)
    - PASSWD_KEY (密码,必填)
    - SERVER_KEY ([server 酱](https://sct.ftqq.com/sendkey) key，用于将脚本结果发送 server 酱通知；选填)

3. 修改 .github/workflows 定时策略 cron

   参考 github action 文档 [CRON](https://docs.github.com/cn/actions/reference/events-that-trigger-workflows#scheduled-events)
    
    ```yml
    schedule:
        - cron: '0 12 * * *'
    ```
    <div align="center">
        <img src="./img/计划任务语法.png" width="80%" align="center" alt="计划任务语法">
    <div>
    
4. 流量转换设置 bin/dukou_checkin.dart
    ```bash
    TransformResult transformResult = await trafficTransform(1024, token);
    ```

5. Action中Enable workflow生效

## 免责
本代码仅用于学习，下载后请勿用于商业用途，并且使用该脚本发生的一切后果与本人无关
