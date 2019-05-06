# td_token

**token详情**

```c++
    struct td_token {
        capi_name contract;  // token对应的合约
        asset total; // token发行总量
        string name; // 项目名称
        string desc; // 项目描述
        string url; // 项目官网
        string logo; // 项目logo
        map<string, string> contacts; // 联系方式
        string white_paper; // 白皮书连接地址
        uint64_t blockchain_id; // 链id
        bool is_sidechain; //是否是侧链token
        bool status; // token状态,是否可进行交易
    }
```