# go-module-test
做一个使用Go实现的project，并且把做好的module上传。之后在另一个project中引用做好的module。
这个project
是做第一步。

## 创建一个module,  name: github.com/wyljpn/go-module-test
```shell
go mod init github.com/wyljpn/go-module-test
go: creating new go.mod: module github.com/wyljpn/go-module-test
```

## 上传
```shell
git commit -m "add Reverse: for v0.1.0"
git tag v0.1.0
git push origin v0.1.0
```

## 在别的go project使用
下载library
```shell
go get github.com/wyljpn/go-module-test@v0.1.0
```

在代码中调用
```go
package main

import (
	"fmt"
	"github.com/wyljpn/git-module-test/stringutil"
)

func main() {
	s := stringutil.Reverse("git-module-test")
	fmt.Println(s)
}

```



