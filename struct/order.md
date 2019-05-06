# td_order

**order详情**

```c++
    struct td_order {
        uint64_t id; // 委托订单id
        capi_name pair; // 委托交易对
        capi_name source_contract; // 源token合约
        capi_name target_contract; // 目标token合约
        capi_name account; // 委托账户名
        capi_name receiver; // 针对主链侧链转账的收款账户
        string type; // 交易类型: limit or market
        asset source_amount; // 源token总额
        asset target_amount; // 目标token总额
        asset price; // 委托价格
        asset source_deal; // 成交的金额(source token)
        asset target_deal; // 成交的金额(target token)
        uint8_t direction; // 委托方向
        uint8_t status; // 订单状态 1: 未成交的新订单 2: 部分成交
        uint64_t create_time;  // 委托时间
    }
```

