#### 概念说明

  指针数组是数组，数组的元素是指针；

  数组指针，指向数组；

#### 示例

```go
package main

import "fmt"

/**
* @author wangpengcheng@ccssoft.com.cn
* @date 2018/5/14 10:52
 */

func main() {

	//指针数组:数组元素是指针
	var x, y = 1, 2
	var a = [...]*int{&x, &y}

	//数组指针
	var z = [...]int{x, y}
	// 值得注意的是go语言中不同长度的数组类型是不一样的，所以声明数组指针的时候一定要注意。
	// 变量是指向数组的指针
	var b *[2]int = &z
	fmt.Printf("a[0]=%d,a[1]=%d;b=%d\n", *a[0], *a[1], *b)
}
```

