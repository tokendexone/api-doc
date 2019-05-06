# td_pair

**交易对信息**

```c++
    struct td_pair {
        capi_name pair; // 交易对
        string name; // 交易对友好名称
        capi_name source_contract; // 源token合约 
        capi_name target_contract; // 目标token合约
        uint8_t source_precision; // 源token的
        uint8_t target_precision;
        string logo; // 冗余字段logo
        asset first; // 今天第一单价
        asset latest; // 最新价
        asset highest; // 最高价
        asset lowest; // 最低价
        asset source_deal; // 源成交量
        asset target_deal; // 目标成交量
        asset sell; // 售出金额(挂单)
        asset buy; // 购买金额(挂单)
        int stat; // 0 价格没有变化 1: 价格上升  -1:价格下降
        uint64_t source_fee; // 万分之1 
        uint64_t target_fee; // 万分之1 
        uint64_t blockchain_id;
        bool is_sidechain;
        uint64_t today;
        bool status;
        uint64_t last_time;
        uint64_t create_time;
    }
```