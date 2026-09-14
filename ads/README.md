# 广告配置

维护者修改 manifest.json 即可更新已接入此地址的版本。当前 enabled 为 false，显示内置招租图。

启用示例（将示例地址替换为实际 HTTPS 地址后再开启）：

```json
{
  "enabled": true,
  "title": "广告标题",
  "imageURL": "https://your-domain.example/banner-v1.jpg",
  "destinationURL": "https://your-domain.example/"
}
```

图片建议 1280×800（16:10），PNG/JPEG，不超过 8 MB，单边不超过 8192 像素。异同比例居中裁切。每次换图建议采用新文件名。

可以添加 expiresAt，格式为 ISO 8601 UTC 时间；到期后恢复默认预览。enabled 设为 false 可以撤下广告。客户端联网后定期检查，最短请求间隔 5 分钟，不是即时推送；不能控制离线客户端或旧版 App。

这里只能配置图片和 HTTPS 跳转链接，不能执行脚本或远程更改用户系统。
