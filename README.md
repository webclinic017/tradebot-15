# tradeBot

### 简介：
```
wss获取源数据单独进程管理
request下单单独进程
策略执行在单独进程
监控代码变动及自动进程独立重启

支持多用户、多币对、多策略同时交易
支持实时盘口模拟交易
支持实盘、沙盒模拟同时交易
支持历史数据回测,可观察k线图表
支持添加多交易所
可分布式部署

非常易于添加自定义策略,初始化3种交易策略:
sma趋势策略
震荡策略
反趋势策略(《裸k线交易法》代码实现)
```

### 配置
```
config目录：
user.py 交易用户开启
public.py 公共环境或代理配置
bitmex.py 交易所及用户api配置
```

### 交易：
`python setup.py`
###### 说明:
```
bitmex交易所直接开启策略即用
其他交易所仿照bitmex配好 k线、成交单、仓位即可
代码逻辑简单，方便新手可直接在strtegy目录下添加一个自己的策略；仿照其他策略吐出 add_order、del_order、update_order即可
币种选择、实盘还是模拟之类的直接在配置中
```

### 回测：
`python test.py`