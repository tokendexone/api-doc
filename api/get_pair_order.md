# 获取交易对的委托订单

#### 获取交易对委托订单(需要根据返回值,根据pair进行过滤)
```shell
cleos -u EOS_RPC_URL get table tokendex1234 tokendex1234 order --index 5
```

#### 返回值
```json
{
  "rows": [{
      "id": 19,
      "pair": "eostdc",
      "source_contract": "eosio.token",
      "target_contract": "tokendexcoin",
      "account": "tokendex3333",
      "receiver": "",
      "type": "limit",
      "source_amount": "4.2143 EOS",
      "target_amount": "1877.1937 TDC",
      "price": "0.00224500 EOS",
      "source_deal": "0.0000 EOS",
      "target_deal": "0.0000 TDC",
      "direction": 2,
      "status": 1,
      "create_time": 1555901942,
      "details": []
    }
  ],
  "more": false
}
```

#### 获取某个账户的委托订单(需要根据返回值,根据account进行过滤)
```shell
cleos -u EOS_RPC_URL get table tokendex1234 tokendex1234 order --index 2 --key-type name -L accountname
```

#### 返回值
```json
{
  "rows": [{
      "id": 19,
      "pair": "eostdc",
      "source_contract": "eosio.token",
      "target_contract": "tokendexcoin",
      "account": "tokendex3333",
      "receiver": "",
      "type": "limit",
      "source_amount": "4.2143 EOS",
      "target_amount": "1877.1937 TDC",
      "price": "0.00224500 EOS",
      "source_deal": "0.0000 EOS",
      "target_deal": "0.0000 TDC",
      "direction": 2,
      "status": 1,
      "create_time": 1555901942,
      "details": []
    }
  ],
  "more": false
}
```

#### 注释

accountname 要查询的账户名

pairname 是交易对，如 esotdc
