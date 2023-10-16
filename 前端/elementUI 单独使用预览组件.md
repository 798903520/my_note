1. 组件内引入 预览组件
```
components:{  
  'el-image-viewer': () => import('element-ui/packages/image/src/image-viewer')  
},
```
2. 使用组件
imgViewerVisible控制显示
imgList 图片预览列表
closeImgViewer 方法内关闭显示
```
<el-image-viewer  
  v-if="imgViewerVisible"  
  :on-close="closeImgViewer"  
  :url-list="imgList" />
```