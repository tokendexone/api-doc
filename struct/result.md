# td_result

**result详情**

```c++
    struct td_result {
        uint64_t id; // 
        uint64_t to_id;
        capi_name pair; // 交易对
        capi_name from; // 来源方
        capi_name to; // 目标方
        uint8_t direction; // 交易方向
        asset price; // 交易价格
        asset source_deal; // 交易源token总额
        asset target_deal; // 交易目标token总额
        asset fee; // 针对来源方的手续费
        uint64_t create_time;
    }
```




