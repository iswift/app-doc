
# 回款日历接口
## 请求url
http://192.168.1.189:8081/app/user/collectDetails

## 请求入参
``` javascript
 {
 	"pageSize": "20",
 	"page": "0",
 	"userId": 6258,
 	"refundDate": "2018-09-11"//回款时间
 }
```


## 响应报文
``` javascript
{
    "calendarList": [//日历集合
        {
            "receivedAmount": 0,//已回款金额
            "pendingAmount": 9740.04,//待回款金额
            "refundDate": "2018-09-11"//回款时间
        },
        {
            "receivedAmount": 0,
            "pendingAmount": 10697.51,
            "refundDate": "2018-09-21"
        }
    ],
    "refundList": [
        {
            "monthIndex": 16,//当前期数
            "totalIndex": 24,//总期数
            "totalAmount": 24.89,//回款总额
            "principal": 22.8,//回款本金
            "interest": 2.09,//利息
            "addInterest": 2.09,//加息
            "refundDate": "2018-09-11",//回款时间
            "actualRefundDate": "2018-09-11",//实际到账时间
            "title": "信投保-37227",//标题
            "state": 0,//状态 0 待回，1 已回
            "stateStr": "待回款"//状态描述
            "assignId": 122//转让id，如果不为空表示是转让回款
        }
    ],
    "todayRefund": {//今日回数据
        "receivedAmount": 0,//已回
        "pendingAmount": 9740.04,//待回
        "refundDate": "2018-09-11"
    },
    "resultCode": 1
}
```












