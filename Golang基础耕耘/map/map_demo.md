# map-demo

> 哈希表是一种巧妙并且实用的数据结构。它是一个无序的key/value对的集合，其中所有的key都是不同的，然后通过给定的key可以在常数时间复杂度内检索、更新或删除对应的value。

## 关注点：

### 1. Map的迭代顺序是不确定的，并且不同的哈希函数实现可能导致不同的遍历顺序。

在实践中，遍历的顺序是随机的，每一次遍历的顺序都不相同。这是故意的，每次都使用随机的遍历顺序可以强制要求程序不会依赖具体的哈希函数实现。如果要按顺序遍历key/value对，我们必须显式地对key进行排序，可以使用sort包的Strings函数对字符串slice进行排序。

### 2. Map的取值，应该先进行if ok 判断，否知容易出现空指针事故。

```go
if value,ok := isMap["key"]; ok {

} else{

}
```

参考链接：

[Go语言圣经-map基本用法](https://books.studygolang.com/gopl-zh/ch4/ch4-03.html)

