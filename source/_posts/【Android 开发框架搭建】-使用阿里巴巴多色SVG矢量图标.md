## 前言

上一个文章[【Android 开发框架搭建】-使用Iconfont-阿里巴巴矢量图标库](/2020/10/20/【Android%20开发框架搭建】-使用Iconfont-阿里巴巴矢量图标库/)介绍了在Android中如何使用阿里巴巴字体文件，但是字体文件只能使用单色的字体图标，在项目中单色图标使用有限这里介绍Android项目阿里巴巴多色SVG矢量图标的使用，丰富我们的应用UI效果减少项目的容量。

## 使用

### 1. 前往阿里巴巴矢量图标下载SVG图片
![iconfont-logo](https://img.alicdn.com/tps/i4/TB1_oz6GVXXXXaFXpXXJDFnIXXX-64-64.ico) [阿里巴巴矢量图标网站](https://www.iconfont.cn/)

<!-- more -->
进入网站登录后，按下方步骤获取SVG图片
点击顶部图标库选择多色图标
![步骤1](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/1.png)

选择喜欢的多色图标库
![步骤2](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/5.png)

选中想要下载的图标点击下载选项
![步骤3](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/2.png)

点击底部SVG下载
![步骤4](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/3.png)

将自己需要的图标都下载好
![步骤5](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/4.png)

### 2. Android项目中使用SVG图标

Google在Android 5.0之后 可以使用VectorDrawable 创建基于XML的SVG图形，创建步骤如下

在项目的res文件夹中 右键drawable/New/Vector Asset
![步骤6](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/6.png)

选择Local File选项,选择svg文件路径点击底部next
![步骤7](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/7.png)

点击finish完成创建
![步骤8](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/8.png)

在drawable文件夹中就会生成对应的SVGxml文件,这里我创建了4个
![步骤9](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/9.png)

xml文件使用方式如下:
注：和正常ImageView添加图片使用一致
```java
<LinearLayout
        android:layout_marginTop="200dp"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <ImageView
             android:src="@drawable/ic_lock"
            android:layout_width="30dp"
            android:layout_height="30dp"/>

        <ImageView
             android:src="@drawable/ic_monitor"
            android:layout_width="60dp"
            android:layout_height="60dp"/>

        <ImageView
             android:src="@drawable/ic_print"
            android:layout_width="90dp"
            android:layout_height="90dp"/>

        <ImageView
            android:src="@drawable/ic_setup"
            android:layout_width="120dp"
            android:layout_height="120dp"/>

    </LinearLayout>

```

Android 5.0之前

需要 在项目的BaseActivity或Application中加入这句代码，即可使用
```java
static {
        AppCompatDelegate.setCompatVectorFromResourcesEnabled(true);
    }
```

附字体图标使用效果图如下
![步骤10](%e3%80%90Android+%e5%bc%80%e5%8f%91%e6%a1%86%e6%9e%b6%e6%90%ad%e5%bb%ba%e3%80%91-%e4%bd%bf%e7%94%a8%e9%98%bf%e9%87%8c%e5%b7%b4%e5%b7%b4%e5%a4%9a%e8%89%b2SVG%e7%9f%a2%e9%87%8f%e5%9b%be%e6%a0%87/10.png)

Demo源码
源码地址 [MiQingWang/AndroidIconTextView](https://github.com/MiQingWang/AndroidIconTextView)