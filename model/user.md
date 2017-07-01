# user

用户表，主要是用来存储用户个人信息

``` javascript
{
  name: {
    // name是唯一的,但是通过id来标识用户
    type:String,
    minlength: 3,
    maxlength: 20,
    required: true,
    trim: true,
    index: true,
    unique: true
  },
   password: {
    //密码使用hash摘要
    type: String,
    required: true
  },
  address: {
    type:String,
  },
  headImgUrl: {
    type: String,
    default: 'http://mixun.magicallu.cn/images/%E5%9F%BA%E6%9C%AC%E8%B5%84%E6%96%99/u354.png'
  },
  desc: {
    type:String,
    default:"这个网站你问我恣辞不恣辞，我当然是恣辞的"
  },
  telephoneNum:{
    type:String
  },
  order:[{
    //对用户订单的引用
    type:Schema.Types.ObjectId,
    ref:"order"
  }]
}
```
## 附带的static函数 

``` javascript
// 
passwordCrypto = (password) => {
  //返回hash摘要
}
// 帮助检查hash前的密码
passwordCheck = (password) => {
  return typeof password === 'string' && password.length >= 6
}
```