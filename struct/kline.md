# kline

**kline详情**

#### 1分钟kline
```c++
    struct td_kline_1m {
        uint64_t id;
        capi_name pair; // 交易对
        asset open; // 开盘价 
        asset high; // 最高价
        asset low; // 最低价
        asset close; // 最终价
        asset volume; // 成交量
        uint64_t time;
    }
```

#### 5分钟kline
```c++
    struct td_kline_5m {
        uint64_t id;
        capi_name pair; // 交易对
        asset open; // 开盘价 
        asset high; // 最高价
        asset low; // 最低价
        asset close; // 最终价
        asset volume; // 成交量
        uint64_t time;
    }
```

#### 30分钟kline
```c++
    struct td_kline_30m {
        uint64_t id;
        capi_name pair; // 交易对
        asset open; // 开盘价 
        asset high; // 最高价
        asset low; // 最低价
        asset close; // 最终价
        asset volume; // 成交量
        uint64_t time;
    }
```


#### 1天kline
```c++
    struct td_kline_1d {
        uint64_t id;
        capi_name pair; // 交易对
        asset open; // 开盘价 
        asset high; // 最高价
        asset low; // 最低价
        asset close; // 最终价
        asset volume; // 成交量
        uint64_t time;
    }
```

#### 1周kline
```c++
    struct td_kline_1w {
        uint64_t id;
        capi_name pair; // 交易对
        asset open; // 开盘价 
        asset high; // 最高价
        asset low; // 最低价
        asset close; // 最终价
        asset volume; // 成交量
        uint64_t time;
    }
```

#### 1月kline
```c++
    struct td_kline_30d {
        uint64_t id;
        capi_name pair; // 交易对
        asset open; // 开盘价 
        asset high; // 最高价
        asset low; // 最低价
        asset close; // 最终价
        asset volume; // 成交量
        uint64_t time;
    }
```
