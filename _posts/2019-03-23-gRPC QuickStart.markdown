---
layout: post
title:  "gRPC Quick Start"
date:   2023年10月22日 星期日 22时57分24秒 CST
categories: Golang gRPC
---
gRPC (gRPC Remote Procedure Calls) 是Google发起的一个开源远程过程调用（Remote procedure call）系统。该系统基于HTTP/2协议传输，使用Protocol Buffers 作为接口描述语言。

# gRPC 简介


# ProtoBuf 使用

```ProtoBuf
message Person {
  string name = 1;
  int32 id = 2;
  bool has_ponycopter = 3;
}
```

# gRPC 在golang中的基本使用

安装依赖

```golang
package tools

import (
    _ "github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-grpc-gateway"
    _ "github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-openapiv2"
    _ "google.golang.org/grpc/cmd/protoc-gen-go-grpc"
    _ "google.golang.org/protobuf/cmd/protoc-gen-go"
)
```
Run `go mod tidy` or 

```bash
$ go install \
    github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-grpc-gateway \
    github.com/grpc-ecosystem/grpc-gateway/v2/protoc-gen-openapiv2 \
    google.golang.org/protobuf/cmd/protoc-gen-go \
    google.golang.org/grpc/cmd/protoc-gen-go-grpc
```

