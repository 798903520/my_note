定义自定义指令
```
directives: {  
  'loadMore': {  
    inserted(el, binding) {  
      const SELECTWRAP_DOM = el.querySelector('.el-select-dropdown .el-select-dropdown__wrap');  
      SELECTWRAP_DOM.addEventListener('scroll', function() {  
        const condition = this.scrollHeight - this.scrollTop <= this.clientHeight;  
        if (condition) {  
          binding.value();  
        }  
      });  
    }  
  }  
},
```

使用自定义指令(loadCountries为达到条件执行的方法)
```
 v-load-more="loadCountries"
```