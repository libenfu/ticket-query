## 12306 车票助手

TicketHelper.

基于`PHP`开发一个12306车票助手程序.


### Blog

博客地址: https://www.helingfeng.com

- [https://www.helingfeng.com/2018/02/18/12306-%E4%BD%99%E7%A5%A8%E6%9F%A5%E8%AF%A2/](https://www.helingfeng.com/2018/02/18/12306-%E4%BD%99%E7%A5%A8%E6%9F%A5%E8%AF%A2/ "https://www.helingfeng.com/2018/02/18/12306-%E4%BD%99%E7%A5%A8%E6%9F%A5%E8%AF%A2/")
- [https://www.helingfeng.com/2018/02/19/12306-%E9%AA%8C%E8%AF%81%E7%99%BB%E5%BD%95/](https://www.helingfeng.com/2018/02/19/12306-%E9%AA%8C%E8%AF%81%E7%99%BB%E5%BD%95/ "https://www.helingfeng.com/2018/02/19/12306-%E9%AA%8C%E8%AF%81%E7%99%BB%E5%BD%95/")

---


### Feature

- 余票查询 
- 验证登录（开发中）
- 订单查询（开发中）
- 账号客户信息获取（开发中）
- 配置抢票任务（规划中）

### Installation

环境要求

- PHP7
- Composer

依赖包安装

```shell
composer install
```

### Usage

```shell
php bin/console

输出
Available commands:
  help                Displays help for a command
  list                Lists commands
 ticket
  ticket:quick-query  查询12306列车余票信息.
```

余票查询命令

```shell
php bin/console ticket:quick-query 北京 上海 2018-02-28


┌──────────────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┬─────────┐
│ STATION_CODE │ GR_NUM │ QT_NUM │ RW_NUM │ RZ_NUM │ TZ_NUM │ WZ_NUM │ YB_NUM │ YW_NUM │ YZ_NUM │ ZE_NUM │ ZY_NUM │ SWZ_NUM │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┼────────┼─────────┤
│ G147         │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ No     │ 1       │
│ G21          │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ No     │ No      │
│ G149         │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ No     │ Yes     │
│ G151         │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ Yes    │ Yes     │
│ G23          │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ Yes    │ 13      │
│ G153         │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ Yes    │ 13      │
│ G155         │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ Yes    │ 5       │
│ G157         │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ Yes    │ 15      │
│ G159         │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ Yes    │ Yes    │ 18      │
│ G7           │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ No     │ No     │ No      │
│ G9           │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ Yes    │ No     │ No      │
│ T109         │ 3      │ --     │ No     │ --     │ --     │ Yes    │ --     │ No     │ No     │ --     │ --     │ --      │
│ D313         │ --     │ --     │ Yes    │ --     │ --     │ No     │ --     │ --     │ --     │ No     │ --     │ --      │
│ D311         │ --     │ --     │ No     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --     │ --      │
│ D321         │ --     │ --     │ Yes    │ --     │ --     │ No     │ --     │ --     │ --     │ No     │ --     │ --      │
└──────────────┴────────┴────────┴────────┴────────┴────────┴────────┴────────┴────────┴────────┴────────┴────────┴─────────┘

```

余票查询帮助

```shell
Arguments:
  from_station          余票列车起点车站?
  to_station            余票列车终点车站?
  date                  余票查询日期[Y-m-d]?

Options:
      --code=CODE       车票类型，普通票/学生票? [default: "普通票"]

```

...

### License

This library is published under The MIT License.

### Thanks

软件作者：何凌枫（helingfeng）