# 获取交易对的价格列表

#### 获取交易对买单价格列表(需要根据返回值pair进行过滤)

```shell
cleos -u EOS_RPC_URL get table tokendex1234 tokendex1234 buystats -L pairname
```
#### 返回值
```json
{
  "rows": [{
      "pair": "eostdc",
      "stats": [{
          "key": "0.00224500 EOS",
          "value": "1877.1937 TDC"
        }
      ],
      "count": 1,
      "source_total": "4.2143 EOS",
      "target_total": "1877.1937 TDC"
    }
  ],
  "more": false
}
```

#### 获取交易对卖单价格列表(需要根据返回值pair进行过滤)

```shell
cleos -u EOS_RPC_URL get table tokendex1234 tokendex1234 sellstats -L pairname
```
#### 返回值
```json
{
  "rows": [{
      "pair": "eostdc",
      "stats": [{
          "key": "0.00025000 EOS",
          "value": "10.0000 TDC"
        },{
          "key": "0.00085000 EOS",
          "value": "10.0000 TDC"
        }
      ],
      "count": 2,
      "source_total": "0.0110 EOS",
      "target_total": "20.0000 TDC"
    }
  ],
  "more": false
}
```

#### 注释

pairname 交易对名称，如 esotdc
