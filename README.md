# openwebui-docker-webdav

`port:8080`

## ENV
```
SYNC_INTERVAL=300
UID=1000
GID=1000
ENABLE_AUTH=True
WEBUI_AUTH=True
ENABLE_OLLAMA_API=False
TZ=Asia/Shanghai
ENABLE_REALTIME_CHAT_SAVE=false
```
```
G_NAME
G_TOKEN
USER_AGENT
WEBDAV_URL # https://jike.teracloud.jp/dav  
WEBDAV_USERNAME # 用户名
WEBDAV_PASSWORD  # 连接密码，第3步获取到的
WEBUI_SECRET_KEY # t0p-s3cr3t
```

## Proxy
```js
export default {
  async fetch(request, env) {
    const url = new URL(request.url);
    url.host = '你的地址'; 
    return fetch(new Request(url, request))
  }
}
```