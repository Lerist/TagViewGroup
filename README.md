# TagViewGroup
Android 仿`小红书`图片标签，实现了图片标签的动画，布局，水波纹，编辑等功能，还可以自定义 Tag。[视频演示地址](http://7vzpfd.com1.z0.glb.clouddn.com/shamuMMB29Klijx12252016215920.mp4)

[![](https://jitpack.io/v/shellljx/TagViewGroup.svg)](https://jitpack.io/#shellljx/TagViewGroup)

![](http://7vzpfd.com1.z0.glb.clouddn.com/ezgif.com-dc9f221590.gif)

#Gradle

**Step 1.**Add it in your root build.gradle at the end of repositories:
```groovy
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```

**Step 2.**Add the dependency
```groovy
dependencies {
	    compile 'com.github.shellljx:TagViewGroup:v1.1'
}
```

#How to use

**1. Define in xml**
```groovy
<com.licrafter.tagview.TagViewGroup
    android:id="@+id/tagViewGroup"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    app:inner_radius="4dp"
    app:line_width="1dp"
    app:radius="8dp"
    app:ripple_alpha="100"
    app:ripple_radius="20dp"
    app:tilt_distance="20dp"/>
```

**2. Or in code**
```groovy
tagViewGroup.setShowAnimator(AnimatorUtils.getTagShowAnimator(tagViewGroup))
        .setHideAnimator(AnimatorUtils.getTagHideAnimator(tagViewGroup))
        .addTagList(tagViewList)
        .setPercent(percentX,percentY)
        .addRipple();
```

**Attributes:**

|attr属性|description 描述|
|:---|:---|
|inner_radius|中心内圆半径|
|radius|中心外圆半径|
|line_width|线条宽度|
|v_distance|圆心到垂直折点的垂直距离|
|tilt_distance|圆心到斜线折点的垂直距离|
|ripple_alpha|水波纹起始透明度|
|ripple_maxRadius|水波纹最大半径|
     
