# Go语言入门第五天（三）

### 接口


```
定义格式
//定义接口
type interface_name interface {
    method_name1 [return_type]
    method_name2 [return_type]
    ....
    method_namen [return_type]
}

//定义结构体
type struct_name struct {
    /* variables */
}

/* 实现接口方法 */
func (struct_name_variable struct_name) method_name1() [return_type] {
    
}

func (struct_name_variable struct_name) method_namen() [return_type] {

}
```

```
package main

type Phone interface {
    call()
}

type Nokia struct {
}

func (nokia Nokia) call() {
    println("Nokia call")
}

type Iphone struct {
}

func (iphone Iphone) call() {
    println("Iphone call")
}

func main() {
    var phone Phone

    phone = new(Nokia)
    phone.call()
    
    phone = new(Iphone)
    phone.call()
}
```
