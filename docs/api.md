# API Reference

[简体中文](api.zh-CN.md) | [Docs Index](README.md)

This inventory is generated from `go doc -short` for the packages in this repository. It is a quick public-surface map; source files and tests remain the authority for exact semantics.

## Packages

### `gnalloy.org/transport-raw`

Package name: `raw`

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
