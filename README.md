# IOS-DSLR-SDK-for-PTP
Canon, NIkon, Sony, Fuji PTP Comand For IOS

iOS 端通过 PTP / PTP-IP 控制佳能 / 索尼 / 尼康相机：拍照、录像、参数控制、媒体下载
一个面向实战的 iOS 相机控制组件与示例 App，统一封装 Canon / Sony / Nikon 的控制流程，支持 PTP（USB/MTP）与 PTP-IP / 厂商远程协议（Sony Remote API）等多种传输方式，覆盖拍照、录像与媒体管理的完整链路。

✨ 功能特性</br>
	•	相机连接</br>
	•	Wi-Fi 直连 / AP / 同网段：mDNS/SSDP/手动 IP 连接</br>
	•	USB-C（部分机型/方式有限制，见兼容性说明）</br>
	•	自动心跳、掉线重连、相机事件订阅（ObjectAdded、PropertyChanged 等）</br>
	•	拍照/录像控制</br>
	•	拍照：单张、连拍、Bulb、曝光包围（AEB/ISO/Shutter 可组合，视机型支持）</br>
	•	录像：开始/停止、模式切换（电影/照片）、剪辑分段（若相机支持）</br>
	•	对焦/测光：单点/多点/AF-S/AF-C 切换、触控对焦（LiveView 模式下）</br>
	•	变焦与镜头控制（电子变焦/电动镜头，取决于机身/镜头能力）</br>
	•	参数设置</br>
	•	曝光三要素：Shutter / Aperture / ISO</br>
	•	白平衡、色温、画质（RAW/JPEG/HEIF）、图像风格</br>
	•	驱动模式（单拍/连拍/定时器）、防抖开关、存储槽位（SD1/SD2）</br>
	•	自定义厂商扩展属性（Vendor Ops / DeviceProp — 以能力协商为准）</br>
	•	实时预览（可选）</br>
	•	LiveView 拉流（MJPEG/H.264，因厂商与机型而异）</br>
	•	低延时渲染、帧率/分辨率协商、拍摄叠层 UI（对焦框、测光点）</br>
	•	媒体管理</br>
	•	文件列表：按时间/类型/容量过滤，增量同步</br>
	•	下载原片/视频（支持分块与断点续传，进度回调）</br>
	•	保存至相册 / App 沙盒 / 自定义相册，自动写入 EXIF/地理位置信息（可选）</br>
	•	删除/保护文件（若相机允许）</br>
	•	工程支持</br>
	•	统一协议抽象：CameraDevice / Transport / CommandQueue</br>
	•	PTP 会话管理、事务序列化、错误重试与超时治理</br>
	•	可插拔编解码（PTP 核心、Sony HTTP/JSON、Nikon/Canon 扩展 OPCodes）</br>
	•	详细日志与抓包（十六进制帧/事件追踪，便于调试厂商差异）</br>

 ✅ 兼容性与平台</br>
	•	iOS / iPadOS：15.0 及以上（建议 16+）</br>
	•	设备：</br>
	•	USB-C 直连：仅在少数组合可行；iOS 对通用 USB 访问有限制，通常需厂商 SDK 或配件方案。推荐优先走 Wi-Fi/热点 方案</br>
	•	相机品牌与协议</br>
	•	Canon：PTP/PTP-IP + 厂商扩展 OPCodes（LiveView/录像等）</br>
	•	Sony：远程控制多走 Sony Camera Remote API（HTTP/JSON+MJPEG）；USB/MTP 控制覆盖有限</br>
	•	Nikon：PTP/PTP-IP + 厂商扩展</br>

实际能力受机型固件影响（尤其是录像控制与 LiveView 编码），以运行时能力协商为准。</br>

🤝 商务合作与技术支持</br>

如果你需要定制开发、二次集成、品牌私有化、机型专项适配，欢迎联系我：</br>
	•	WeChat：+86 15083516765</br>
	•	Email：wujian7463@gmail.com</br>

欢迎在 Issue 中提交需求/BUG，也可以直接加我沟通详细场景（直播/活动摄影棚/相机矩阵/视频采集柜等）。</br>
