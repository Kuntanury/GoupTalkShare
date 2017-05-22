#GoupTalkShare


##2016年8月23日

![iamge2016082301](https://github.com/Kuntanury/GoupTalkShare/blob/master/images/2016082301.png)

关于上图原型实现的讨论：
>collectionview实现，cell上面加image和textview，用cell的代理返回编辑的数据

##2017年5月22日

出现没有文件名的 linker command failed with exit code 1错误

>把Other Linker Flags下的属性全部删除，重新添加$(inherited)

##2017年1月6日

同一控制器里不同的控件设置了相同的tag值 会报错吗
>不会报错 tag在同一层视图的话 会优先获取先add的唯一视图 不在同一层不互相影响
