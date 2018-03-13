# 链家网爬虫
### 功能介绍
- 获取链家网小区房价数据。如果好用，请star。
- 城市 city, 区县 district, 板块 area, 小区 xiaoqu。
- 每个版块一个csv文件。
- 内容格式：采集日期,所属区县,板块名,小区名,挂牌均价,挂牌数
- 内容如下：20180221,浦东,川沙,恒纬家苑,32176元/m2,3套在售二手房

### 运行
- python xiaoqu.py 根据提示输入城市代码，回车确认
```
hz: 杭州, sz: 深圳, dl: 大连, xm: 厦门
gz: 广州, bj: 北京, cd: 成都, jn: 济南
sh: 上海, tj: 天津, qd: 青岛, su: 苏州
cq: 重庆, wh: 武汉, hf: 合肥, nj: 南京
```

### 性能
- 300秒爬取上海市207个版块的2.7万条数据，平均每秒90条数据。
```
Total crawl 207 areas.
Total cost 294.048109055 second to crawl 27256 data items.
```

### 结果存储
- 根目录下建立data目录存放结果数据文件
- 存储目录为 data/lianjia/city/date

### 更新记录
- 2018/03/10 自动获取城市的区县列表，现在支持16个城市小区数据爬取
- 2018/03/06 支持北京二手房小区数据采集
- 2018/02/21 应对链家前端页面更新，使用内置urllib2代替第三方requests库,提升性能，减少依赖
- 2018/02/01 支持上海二手房小区数据采集

