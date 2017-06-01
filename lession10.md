# Go语言入门第四天（五）

### 结构体

```
//定义格式
type struct_variable_type struct {
    member definition
    .....
}
```



```
//例子
package main


type Books struct {
    name string
    author string 
}

func (book *Books) setAuthor(author string) {
    book.author = author
}

func (book *Books) setName(name string) {
    book.name = name
}

func main() {
    var book1 = Book{"zbook1"， "zb"}
    prinln(book1.name)

    book1.setName("zbook2")
    book1.setAuthor("zbx")
    
    println(book1.name, book1.author)
}
```
