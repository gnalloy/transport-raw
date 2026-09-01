# API 参考

[English](api.md) | [文档索引](README.zh-CN.md)

本清单由本仓库 package 的 `go doc -short` 生成，用于快速查看公共面。精确语义以源码和测试为准。

## 包

### `gnalloy.org/transport-raw`

包名：`raw`

```text
const ProtocolICMP = 1 ...
var ErrInvalidAddress = errors.New("gnalloy/transport/raw: invalid address") ...
type Address struct{ ... }
type Addressed struct{ ... }
type AddressedMessageEncoder interface{ ... }
type AllocatorFactory func(loop *transport.EventLoop) (buffer.Allocator, error)
    func NewMmapAllocatorFactory(cfg buffer.MmapAllocatorConfig, fallbackToHeap bool) AllocatorFactory
type Config struct{ ... }
    func DefaultConfig() Config
type Family uint8
    const FamilyIPv4 Family = iota + 1 ...
type MessageToPacketEncoder struct{ ... }
    func NewMessageToPacketEncoder(encoder AddressedMessageEncoder) *MessageToPacketEncoder
    func NewMessageToPacketEncoderFunc(accept func(any) bool, ...) *MessageToPacketEncoder
type Packet struct{ ... }
type PacketEncoder struct{}
    func NewPacketEncoder() *PacketEncoder
type PacketPayloadDecoder interface{ ... }
type PacketToMessageDecoder struct{ ... }
    func NewPacketToMessageDecoder(decoder PacketPayloadDecoder) *PacketToMessageDecoder
    func NewPacketToMessageDecoderFunc(accept func(Packet) bool, ...) *PacketToMessageDecoder
type Server struct{ ... }
type Transport struct{ ... }
    func NewTransport(cfg Config) *Transport
```
