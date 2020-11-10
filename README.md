# 数据监听

入口：init -> state

## 源码总结：

- props的key最终都会转为驼峰式命名
- 转驼峰的时候使用了cache的高阶函数进行缓存，提高性能
- data属性不能与props和method重名，因为最后都会代理到vm实例下
- data属性不能以_或者$开头，因为可能会与vue的预置属性冲突，从而不能挂载到vm上，但通过this.data._xxx还是可以访问到