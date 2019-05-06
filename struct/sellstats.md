# td_sell_stat

**交易对卖单价格列表**

```c++
    struct td_sell_stat {
        capi_name pair; // 交易对
        std::map<asset, asset> stats; // price(价格) -> total (总的目标token委托额)
        uint64_t count; // 委托数量
        asset source_total; // 所有委托source_token的总额
        asset target_total; // 所有委托target_token的总额
    }
```

