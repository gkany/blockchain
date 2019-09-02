# 1. 稳定币
稳定币之所以称为稳定币，就是需要它的价格要保持相对的稳定。

稳定币的作用就是充当数字货币和法币一个交换中介。

人们可以先将手中的法币汇给相关的机构，兑换成“稳定币”，然后再进行其他数字货币的自由交易。

## 1.1 USDT 



# 2. Bitshare喂价



1. 自定义智能资产
* 创建资产
create_asset nathan MYMPA 5 {"issuer_permissions": 511,"flags": 128,"core_exchange_rate":{"base":{"amount":1,"asset_id":"1.3.0"},"quote":{"amount":1,"asset_id":"1.3.1"}}} {"new_feed_producers":[],"feed_lifetime_sec":120} true

create_asset nicotest1 MYMPA 5 {"issuer_permissions": 511,"flags": 128,"core_exchange_rate":{"base":{"amount":1,"asset_id":"1.3.0"},"quote":{"amount":1,"asset_id":"1.3.1"}}} {"new_feed_producers":[],"feed_lifetime_sec":120} true

* 设置喂价人
update_asset_feed_producers MYMPA [in.abit,dele-puppy] true

update_asset_feed_producers MYMPA [assetfeed1, assetfeed2] true

* 喂价
publish_asset_feed in.abit MYMPA {"settlement_price":{"base":{"amount":50000,"asset_id":"1.3.662"},"quote":{"amount":1000000000,"asset_id":"1.3.0"}},"core_exchange_rate":{"base":{"amount":100000,"asset_id":"1.3.0"},"quote":{"amount":10000,"asset_id":"1.3.662"}}} true

publish_asset_feed assetfeed1 MYMPA {"settlement_price":{"base":{"amount":50000,"asset_id":"1.3.1"},"quote":{"amount":1000000000,"asset_id":"1.3.0"}},"core_exchange_rate":{"base":{"amount":100000,"asset_id":"1.3.0"},"quote":{"amount":10000,"asset_id":"1.3.1"}}} true

1. 预测市场
* 创建资产
create_asset nathan ASSETNAME 5 {"issuer_permissions": 511,"flags": 128,"core_exchange_rate":{"base":{"amount":1,"asset_id":"1.3.0"},"quote":{"amount":1,"asset_id":"1.3.1"}}} {"new_feed_producers":[],"is_prediction_market":true} true


* 结算（不知道专业术语是什么，意思就是结束这个预测市场）
global_settle_asset ASSETNAME {"base":{"amount":1,"asset_id":"1.3.663"},"quote":{"amount":1,"asset_id":"1.3.0"}} true

其中base是预测市场资产，quote是货币资产（例子里是BTS），asset_id是对应的资产id，base amount / quote amount 设 1/1就是赢，0/1就是输，1/2就是平局；base amount值应该不能比quote大。

注意事项
1.资产代码后面的数字，是小数位数。比如BTS的小数位数是5，CNY是4。预测市场的小数位数要与下注货币小数位数相同。注意先想清楚，这个一旦创建就不能修改的。

2.权限是用来限制资产发行人的。请注意，这个非常重要：开启权限才能修改旗标；权限一旦关闭很难再次开启（不信去问巨蟹）。现在界面里，默认是黑色，表示开启。

3.另外请注意，那个“手续费汇率”也非常重要。因为创建资产花的BTS手续费，有一半会进手续费池，等于别人可以按你设置的汇率，用你的资产来买池里的BTS。有个哥们跑了个机器人，专偷设错汇率的资产的手续费池。