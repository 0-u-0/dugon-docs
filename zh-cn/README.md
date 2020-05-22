# 目标：
- 分布式流媒体服务器（已完成服务器级联功能，目前已可负载均衡）
- 分布式信令服务器（分布式已ok，）
- Web SDK，Typescript（基本完成 90%，剩下些许api和功能），[API Doc](http://webapi.dugon.one/) （已上线，但接口不全） ，[Demos](https://demo.dugon.one/) （已上线），浏览器兼容性（目前只支持Chrome）
- iOS SDK，Swift（60%，基本跑通，但是服务器改了些接口，目前连不通了。。），API Doc(无)，Demos(无)
- Android SDK，Java（20%，架子基本搭好，加逻辑就ok了），API Doc(无)，Demos(无)。

# 未来
- 完善文档，[https://dugon.one](https://dugon.one)，Markdown可。
- 目前媒体服务器是基于 [mediasoup](https://github.com/versatica/mediasoup)，未来想基于 [pion/webrtc](https://github.com/pion/webrtc)自己开发流媒体服务器。
- 其他端SDK，如 Windows，MacOS，Raspberry 等。

# 设计
- 分布式整体基于 [NATS](https://nats.io/) （分布式消息队列）设计。
- 为了快速部署和迁移，部署使用`Docker`，镜像已上线 `dockerhub` 。目前信令 `Docker` 镜像 `14M`；流媒体 `Docker` 镜像 `1.6G` ，流媒体服务器会逐渐使用 `Go` 重写，减小镜像，预计能减到 `80M`。
