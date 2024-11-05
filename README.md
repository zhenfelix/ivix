# ivix
## Module Updated #5
- [Module Updated #5](https://github.com/Alexdachen/ivix/issues/5)
- [VIX replication](https://vix.readthedocs.io/en/latest/#rff6015b8fcab-1)

## data source
- [上证50vix](https://vinsight.shnyu.edu.cn/implied_moments.php?hs300=out300_vix_30&a50=out_vix_30&zz1000=out_vix_30)
- [银行间拆借利率](https://github.com/akfamily/akshare/blob/main/docs/data/interest_rate/interest_rate.md#%E9%93%B6%E8%A1%8C%E9%97%B4%E6%8B%86%E5%80%9F%E5%88%A9%E7%8E%87)
- [期权概况-获取期权合约信息](https://www.joinquant.com/help/api/help#JQData:%E6%9C%9F%E6%9D%83%E6%A6%82%E5%86%B5)
- [期权行情日数据-上证50指数-上交所-根据合约信息获取日行情](https://akshare.akfamily.xyz/data/option/option.html#id25)



## 中国波指的计算

vix指数的计算方法如下（ivix也是一样）：

[vix指数的简单计算介绍](http://vix.readthedocs.io/en/latest/)

[CBOE,vix白皮书](http://www.cboe.com/products/vix-index-volatility/vix-options-and-futures/vix-index/the-vix-index-calculation)

中国波指，作为一个波动率指数，也叫情绪指数，具有一定的预测作用。

* 目前是用于计算历史日间的中国波指。

* 数据截止日期为2018年7月5日的。需要新的数据自己进行获取了。

画图模块是用pyecharts库，需要安装一下pyecharts.
```
pip install pyecharts
```
![image](https://github.com/Alexdachen/ivix/blob/master/%E4%B8%AD%E5%9B%BD%E6%B3%A2%E6%8C%87.png)

如图，计算出来的vix指数结果以及原始中证公司公布出来的vix指数对比，可见大部分是一致的，当然也有小部分是不一致的，造成原因可能是原始数据质量的问题了。但是用这个方法去替代不再发布的vix指数还是可行的，2018年2月14号之后不再发布中国波指了。

后续将会更新实时计算日内的中国波指；同时也会把wind接口全部换成爬虫接口。


# License
MIT

