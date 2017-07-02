# 订单

``` javascript
{
  goods:{
    type:Schema.Types.ObjectId,
    ref:"goods"
  },
  num:{
    //件数
    type:Number
    required: true
  },
  address:{
    //收货地址
    type:String,
    required: true
  },
  status:{
    //代表订单的状态
    type:Number,
    default:0
  },
  express:{
    //快递
    type:String,
    required: true
  },
  expressId:{
    //快递号
    type:Number,
    required:true
  }
}
```

订单的状态：
  - -1 ： 订单被取消
  - 0 ： 订单已提交
  - 1 ： 订单已发货
  - 2 ： 订单已被确认收货，订单完成