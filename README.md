# RN-CircularProgress
ReactNative 圆形进度条

![image.png](https://upload-images.jianshu.io/upload_images/23011-5c2d67f5f38bbc79.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
> 思路 绘制两个圆环叠加，改变上部圆环的填充色~

>技术点：需要`ART`，`iOS`和`Android`自行导入

```
Progress.publicFunction = {
    setProgress: PropTypes.func, // 设置进度 取值范围 0 - 1
};

Progress.propTypes = {
    radius: PropTypes.number, // 半径
    annularHeight: PropTypes.number, // 内环高度
    startAngle: PropTypes.number, // 开始角度 0 - 1
    currentAngle: PropTypes.number, // 当前角度 0 - 1
    bgColor: PropTypes.string, // 内环背景填充颜色
    selectColor: PropTypes.string, // 内环背景选中填充颜色
};

Progress.defaultProps = {
    radius: 50,
    annularHeight: 2,
    startAngle: 0, // 0 - 1
    currentAngle: 0, // 0 - 1
    bgColor: '#f5f5f5',
    selectColor: 'blue'
};
```

# 使用一：只要圆环效果
```
 <Progress ref={(ref)=>this.progress = ref} />
```
# 使用二：圆环+内部视图
```
 <Progress ref={(ref)=>this.progress = ref} >
    <Text>你好</Text>
    ......
</Progress>
```
# 改变进度
```
this.progress.setProgress(0.3)  // 0 - 1
```
