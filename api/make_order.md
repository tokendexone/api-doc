## 下单

#### 说明

买单及卖单是根据pair的转账方向进行判断的.

#### memo字段解析

memo是由英文逗号来分隔开的几个字段。

格式如下: type,pair,price

type值为limit和market,limit是限价交易,market是市价交易

pair是要进行交易的交易对.如 eostdc, eos是

price是交易价格.对应真实的交易价格,如0.0012.最高支持8位小数位,超出则进行截取处理

#### 关于limit及market

* limit 只有卖方跟买方价格完全匹配才能进行成交。当存在多个相同价格的委托时,依据创建的时间从早到晚进行成交。
* market 只有存在对应委托订单时才能成交,未成交的金额立即返回账户内，卖单依据买单价格从高到低的顺序成交，买单依据卖单价格从低到高的顺序成交。

#### 事例

**以0.001 EOS的价格花费1.0000 EOS买入, 获得对应TDC数量的代币**
```shell
cleos -u EOS_RPC_URL push action eosio.token transfer '["your account","tokendex1234","1.0000 EOS","limit,eostdc,0.001"]' -p your account
```
**以0.002 EOS的价格卖出1000.0000 TDC, 获得对应数量的EOS**
```shell
cleos -u EOS_RPC_URL push action tokendexcoin transfer '["your account","tokendex1234","1000.0000 TDC","limit,eostdc,0.002"]' -p your account
```

**花费1.0000 EOS, 根据市价由低到高的顺序买入对应数量的TDC**
```shell
cleos -u EOS_RPC_URL push action eosio.token transfer '["your account","tokendex1234","1.0000 EOS","market,eostdc"]' -p your account
```
**卖出1000.0000 TDC, 根据市价由由高到低的顺序买入对应数量的EOS**
```shell
cleos -u EOS_RPC_URL push action tokendexcoin transfer '["your account","tokendex1234","1000.0000 TDC","market,eostdc"]' -p your account
```