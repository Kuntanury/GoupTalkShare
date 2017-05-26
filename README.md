# GoupTalkShare

## 2017年5月22日

出现没有文件名的 linker command failed with exit code 1错误

>把Other Linker Flags下的属性全部删除，重新添加$(inherited)

## 2017年5月23日

hidesBottomBarWhenPushed = YES 底部工具栏延迟消失

>被推出界面的底部约束为Bottom Layout Guide，更新底部约束对象为Superview

## 2017年5月26日

同一ViewController A中两个ContainerView a b切换，在b所在的ViewController B 用 pushViewController方法，再pop回的时候，A中会自动切回显示a页面。用KVC也无法监视到变化情况发生在哪里。

>
````` 
-(void)viewDidAppear:(BOOL)animated {
    [b removeFromSuperview];
    [self performSelector:@selector(relayoutSubviews) withObject:nil afterDelay:0.1];
}

-(void)relayoutSubviews {
    [self.view addSubview:b];
    [b setFrame:CGRectMake(-SCREEN_WIDTH, 0, SCREEN_WIDTH, SCREEN_HEIGHT-64)];
    [a setFrame:CGRectMake(0, 0, SCREEN_WIDTH, SCREEN_HEIGHT-64)];
}
````` 
