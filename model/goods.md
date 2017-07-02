# 商品表

``` javascript
{
  name:{
    type:String,
    required: true
  },
  price:{
    type:Number,
    required: true
  },
  //购买商品时，商品不同的选项，比如32G，黑色，联通
  selection:Schema.Types.Mixed,
  //商品的详细配置
  configuration:Schema.Types.Mixed
  //展示给用户看的商品样子的图片（一张）
  pic:{
    type:String,
    reqiure:true
  },
  //商品的详细的宣传图片列表
  detailPicList:[
    type:String,
  ],
  //商品是否下架，默认为false，上架
  disable:{
    type:Boolean,
    default:false,
  }
}
``` 

selection的数据大体如下
``` javascript
{
  "颜色":["黑色"，"白色"]，
  "内存":["23G"]  
}
```
configuration:
``` javascript 
{
  "配置":"高端",
  "":"",
}
```






