# App新特性页面
使用方法很简单，直接把KSGuaidView文件夹拖到工程然后稍微修改一下文件夹内的```KSGuaidProperty.plist```内容即可<br>
<br/>

## KSGuaidProperty.plist文件介绍:<br/><br/>
 ```kImageNamesArray```
<br/>
图片数组的Key,值是一个NSArray 里面包含了要显示新特性的图片的名字，这些图片需要添加在Assets.xcassets目录内。<br/><br/>
### ```kLastNullImageName```
<br/>
如果要实现最后一张图片滑动去除的效果(动图二),需要在上一个key里面的数组最后添加这个key作为最后一张图片的name。<br/>
注意:如果用这种方式退出，是不会显示"立即体验"类似的按钮。<br/>
### ``` kHiddenBtnImageName```
<br/>
"立即体验"按钮的图片名称，如果想在最后一张图片上添加一个体验按钮(如图一),则需要指定这个图片的名字，按钮大小会跟随图片的大小设定。<br/>
如果在```kImageNamesArray```最后添加了```kLastNullImageName```，即使指定了```kHiddenBtnImageName```不过也不会起作用。<br/>
### ```kHiddenBtnCenter```
<br/>
"立即体验"按钮的相对屏幕的位置，value是```{x,y}```字符串类型的point。x,y的取值范围为[0,1],```{0.5,0.5}```是屏幕中心。
