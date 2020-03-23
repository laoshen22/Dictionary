# 字典 Dictionary

用户操作分为**事件`event`**进行埋点，包括：逻辑行为`LOGIC`，检测行为`TEST`，登录行为`LOGIN`，列表加载行为`LIST`，观看行为`WATCH`，收藏行为`FAVORITE`，搜索行为`SEARCH`，分享行为`SHARE`，购买行为`PAY`。每个事件会有**具体行为`data.action`**来描述。

## 公共变量 common variables
    {
    "event": "WATCH",     // 事件 
    "@timestamp": "2020-03-20T16:00:15.930Z",    
    "syncTimes": 1,
    "deviceID": "2279c4e3e78d8e2",      
    "product": "dc0d5f2d84284c8b670c1515376a1039",   //产品
    "isNewbee": 0,   //是否新用户 1=是，0=不是，-1=unknow
    "systemVersion": "7.1.1",   //手机系统版本
    "arrLength": 2,  
    "reportIndex": 65,   //行为顺序， eg：第65个行为
    "codeVersion": "v56",  
    "isVip": 0,   //是否购买会员 1=是，0=不是，-1=unknow
    "appVersion": "3.1.0",
    "ip": "183.213.172.207",
    "proxyId": -1,      
    "device": "OPPO A83" 
    }


## TEST 
    
    //request-cdn video commute successful/not
    "event": "TEST",
    "data": {
      "action": "RESOURCE",
      "costRes": 1,  //request-cdn time, second
      "state": 1,  //successful=1, failure=0
      "speed": 3627,  //successful=1, failure=0
      "lastEventTime": 0   //time between current event and last event
    }
    
    //request-cdn image commute successful/not
    "data": {
      "action": "IMAGE",
      "costRes": 0,
      "state": 1,
      "lastEventTime": 0
    }
   
## LOGIN
    //open app remark
    "event": "LOGIN",
    "data": {
      "parent": 1,   //who share it to user
      "lastEventTime": 2
    }
    
## WATCH


    大家来完善