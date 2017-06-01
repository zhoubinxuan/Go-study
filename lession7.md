# Go语言入门第四天（二）

### 函数与方法

```
//函数定义格式
func function_name( [parameter_list] ) [return_types] {
    //函数体
}
```


```
//例子1
package main

func main () {
    a1, a2 := testFunc("123", "1234")
    println(a1, a2)
    getPonter(&a1, &a2)
	println(a1, a2)
	
    nextNumber = getSequence(3)
    println(nextNumber)
    println(nextNumber)
    println(nextNumber)
}

func testFunc(a1, a2 string) (string, string) {
    return a1, a2
}

func getPonter(a1 *string, a2 *string) {
	*a1 = "3"
	*a2 = "4"
}

func getSequence(i int) func() int {
    return func() int {
        i += 1;
        return i
    }
}

```


```
//方法定义格式
func (variable_name variable_data_type) function_name() [return_type] {
    //函数体
}

```


```
例子2
package main

func main() {
    var c1 Circle
    c1.radius = 10.00
    println(c1.getArea())
}

type Circle struct {
    radius float64
}

func (c Circle) getArea() float64 {
    return 3.14 * c.radius * c.radius
}

```









