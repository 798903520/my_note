```
let pages = getCurrentPages(); //获取所有页面栈实例列表
let prevPage = pages[pages.length - 2]; //上一页
prevPage.$vm.selectData.type = this.selectType;
prevPage.$vm.selectData.data = data;
uni.navigateBack({
    delta: 1,
});
```