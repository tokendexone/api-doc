# 取消订单

#### 取消单个订单

```shell
cleos -u EOS_RPC_URL push action tokendex1234 cancelorder '["your account","order id"]' -p your account
```
#### 取消所有订单

```shell
cleos -u EOS_RPC_URL push action tokendex1234 cancelall '["your account",""]' -p your account
```

#### 取消某个交易对的所有订单

```shell
cleos -u EOS_RPC_URL push action tokendex1234 cancelall '["your account","pair name"]' -p your account
```

#### 注释

your account 是进行委托的账户名

order id 是订单id.每个委托都会有id对应

pair name 是交易对，如 esotdc
