# AjaxFileUpload
A jQuery plugin, support asynchronous file upload and asynchronous response (based on HTTP 1.1 chunked protocol)

jQuery异步文件上传插件，支持以下功能：
* 实现前端异步文件上传（基于iframe）。
* 支持异步响应结果（基于Http 1.1 chunked协议），用于返回后端文件处理进度。主要用于数据导入应用场景（如：显示Excel文件导入进度）

###Examples
```js
$.ajaxFileUpload({
  url: '/upload.html',
  secureuri: false,
  fileElementId: 'fileElementId',
  dataType: 'json',
  isAsyncResponse: true,  // 使用异步响应结果
  success: function(data, status) {
    //show progress
  },
  complete:function(data, status) {
    //show finish
  }
});
```
