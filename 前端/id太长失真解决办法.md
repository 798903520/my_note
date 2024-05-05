正则替换为字符串

```
const convertedJsonString = data.replace(/"(\w+)":(\d{15,})/g, '"$1":"$2"'); return JSON.parse(convertedJsonString);
```