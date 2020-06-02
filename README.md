# learning-webRTC
学习learning webRTC一书，发现示例代码下载后不能正常运行（chrome 版本 83.0.4103.61 正式版本 64 位）查看接口文档后做了修改，保存于此

修改摘要

1、流问题
```
// video.src = window.URL.createObjectURL(stream);
video.srcObject = stream
```

2、offer、answer

```
aPromise = myPeerConnection.createOffer([options]);
myPeerConnection.createOffer(successCallback, failureCallback, [options])

aPromise = RTCPeerConnection.createAnswer([options]);
RTCPeerConnection.createAnswer(successCallback, failureCallback[, options]); 

```