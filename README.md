<p align="center">
  <img src="https://s1.ax1x.com/2022/05/24/XPx1tx.png" width="200" height="200" alt="">
</p>
<div align="center">
<h1> 新 B 站粉丝牌助手
</h1>
<p>当前版本：0.1.0</p>
 </div>

**TODO**

- [x] 每日直播区签到
- [x] 每日点赞3次直播间 （200*3 亲密度）
- [x] 每日分享5次直播间  （100*5 亲密度）
- [x] 每日弹幕打卡            （100 亲密度）
- [x] 多账号支持
- [ ] 每日观看30分钟  
- [ ] 微信推送通知

<small>ps: 新版B站粉丝牌的亲密度每一个牌子都将单独计算 </small>

---

### 使用说明  

##### 环境需求：Python 版本大于 3.8

> 克隆本项目 安装依赖

```shell
git clone https://github.com/XiaoMiku01/fansMedalHelper.git
cd fansMedalHelper
pip install -r requirements.txt
```

> 获取B站账号的 access_key  

...

> 填写配置文件  users.yaml

```shell
vim users.yaml
```

```yaml
USERS:
    - access_key: XXXXXX  # 注意冒号后的空格 否则会读取失败
      shared_uid: 123,456 # 需要分享房间的房主UID！不是房间号！ 多个用逗号分隔,最多28个

    - access_key: 
      shared_uid: 
    # 多用户以上格式添加
```

> 运行主程序 

```shell
python main.py
```

> 效果图

[![XiifQP.md.png](https://s1.ax1x.com/2022/05/24/XiifQP.md.png)](https://imgtu.com/i/XiifQP)

---

### 注意事项

- 本脚本暂时没有集成定时模块 还需要用户定时运行  
- 由于B站分享接口并不是每次分享都会加亲密度，它会有10分钟的CD，所以设置一个拿满500需要40分钟，以此类推，但是得益于Python3的异步机制，多个账号将并发完成任务，例如：A账号设置了2个房间的分享任务，B账号设置了1个，所需时间为90分钟。所以一天24小时最多可以拿满28个房间的分享亲密度

---

### 赞助

![](http://i0.hdslb.com/bfs/album/c267037c9513b8e44bc6ec95dbf772ff0439dce6.jpg)