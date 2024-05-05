```
formatter: (params) => {  
  let data = '';  
  for (let item of params) {  
    data =  
      data +  
      `<span style="display: flex;width:auto "><span style="width:70px">${item.marker}${item.seriesName}</span><span style="width:70px">订单数: ${item.data.orderNum}</span><span style="width:80px">金额: ${item.data.value}</span></span>`;  
  }  
  return data;  
},


//params内有所有数据,自定义拼接 设置的series data内是一个对象 需要渲染为折线的数据赋予value值
for (let item of salesKeys) {  
  let seriesItem: any = {  
    name: item,  
    type: 'line',  
    symbol: 'circle',  
    data: data.orderDataList[item],  
  };  
  dailyOrderAmount_option.series.push(seriesItem);  
}  
option = dailyOrderAmount_option;
```