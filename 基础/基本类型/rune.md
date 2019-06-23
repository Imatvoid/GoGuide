## 基本类型


bool

string

int  int8  int16  int32  int64
uint uint8 uint16 uint32 uint64 uintptr

byte // uint8 的别名

rune // int32 的别名 代表一个Unicode码

float32 float64

complex64 complex128

```go
import (
	"fmt"
	"math/cmplx"
)

var (
	ToBe   bool       = false
	MaxInt uint64     = 1<<64 - 1
	z      complex128 = cmplx.Sqrt(-5 + 12i)
)

func main() {
	const f = "%T(%v)\n"
	fmt.Printf(f, ToBe, ToBe)
	fmt.Printf(f, MaxInt, MaxInt)
	fmt.Printf(f, z, z)
}
-------------------------------------------
bool(false)
uint64(18446744073709551615)
complex128((2+3i))
```








## rune

在各个方面基本等于int32,说成int32的别名也不算错,用来表示一个unicode 码点,也就是一个数字。

```go
    fmt.Printf("%T \n", rune)
    >> int32
```


```go
 	s := "我"
 	r := []rune(s)
 	fmt.Println(r)
```

