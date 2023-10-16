发送消息的页面

```
page A

const content = document.querySelector('#content')
        const btn = document.querySelector('#btn')
 
        const broadCastChannel = new BroadcastChannel('load');
                btn.onclick=function(){
                    broadCastChannel.postMessage({
                        value:content.value
                    })
                }
```


接受消息的页面
```
page B

const broadCastChannel = new BroadcastChannel('load');
        broadCastChannel.onmessage = function (e) {
            console.log(e.data);
        }
```