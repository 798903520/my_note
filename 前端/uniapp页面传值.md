父页面内
```
onShow(){
    // Edit是根据跳转过去的type
    uni.$once('getDataEdit' ,(data)=>{
                 this.backData(data)
            });
  },
```

子页面通过emit传递
```
uni.$emit(`getDataEdit` , data);
 uni.navigateBack()
```