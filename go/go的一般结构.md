## go的一般结构

```go
// 当前程序的包名
package main

// 导入其他包
import  "fmt"

// 常量定义
const PI = 3.14


// 全局变量的声明和赋值
var name = "gopher"

// 一般类型声明
type newType int

// 结构的声明
type gopher struct{}

// 接口的声明
type golang interface{}

var x, y int
var (  // 这种因式分解关键字的写法一般用于声明全局变量
    a int
    b bool
)

var c, d int = 1, 2
var e, f = 123, "hello"

//这种不带声明格式的只能在函数体中出现
//g, h := 123, "hello"

// 由main函数作为程序入口点启动有且只有一个
func main() {
    g ,h :=123,"hello"//不需要使用var，改用简洁方式的定义，但是他只能在函数内使用，且使用var 定义之后不可在使用：=进行定义，否则会出错
    fmt.Println("Hello World!")
}
```