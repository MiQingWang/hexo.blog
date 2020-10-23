
## 前言

在项目中经常需要用到一些小图标，避免需要切图或者往项目资源中导入大量图标资源。我们可以使用字体矢量图标来减少资源、适配更方便，这里介绍Android项目阿里巴巴矢量字体图标的使用。

## 使用

### 1. 前往阿里巴巴矢量图标下载字体文件
注：字体只支持单色图标哦，如项目需要使用多色图标可以使用SVG矢量图标，后续章节再介绍Android中如何使用阿里巴巴矢量图标SVG方式的。

![iconfont-logo](https://img.alicdn.com/tps/i4/TB1_oz6GVXXXXaFXpXXJDFnIXXX-64-64.ico) [阿里巴巴矢量图标网站](https://www.iconfont.cn/)

进入网站登录后，按下方步骤获取字体文件
点击资源管理我的项目
![步骤1](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/1.png)
进入我的项目点击右上方加号图标新建项目
![步骤2](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/2.png)
填写项目、项目描述后点击新建
![步骤3](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/3.png)
建好项目后回到首页，点击顶部导航栏中图标库，点击官方图标库选择喜欢的图标模板库
![步骤4](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/4.png)
进入喜欢的图标模板库后选择喜欢的图标，点击加入购物车
![步骤5](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/5.png)
图标选择完毕点击右上角购物车，进入购物车页面
![步骤6](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/6.png)
确认图标正确，点击添加至项目，选择一开始新建的项目点击确定
![步骤7](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/7.png)
确认选择的项目中图标是否正确，点击下载至本地
![步骤8](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/8.png)
解压下载的资源，复制iconfont.ttf
![步骤9](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/9.png)

### 2. Android项目中使用阿里巴巴矢量图标字体文件

在Android项目的assets目录中添加iconfont.ttf的字体文件
![步骤10](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/10.png)
然后在项目中新建一个继承AppCompatTextView的自定义TextView代码如下:
```python
public class IconTextView extends AppCompatTextView {
    public IconTextView(Context context) {
        super(context);
        init(context);
    }

    public IconTextView(Context context, @Nullable AttributeSet attrs) {
        super(context, attrs);
        init(context);
    }

    public IconTextView(Context context, @Nullable AttributeSet attrs, int defStyleAttr) {
        super(context, attrs, defStyleAttr);
        init(context);
    }

    private void init(Context context) {
        //设置字体文件
        this.setTypeface(Typeface.createFromAsset(context.getAssets(),"iconfont.ttf"));
    }
}
```
自定义TextView创建完成后我们就可以使用字体图标了使用方式如下:
```python
<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <项目包名.IconTextView
        android:text="&#xe6eb;"
        android:textSize="30dp"
        android:textColor="@color/black"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <项目包名.IconTextView
        android:text="&#xe6ef;"
        android:textSize="50dp"
        android:textColor="@color/colorPrimary"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <项目包名.IconTextView
        android:text="&#xe6f0;"
        android:textSize="100dp"
        android:textColor="@color/colorAccent"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

</LinearLayout>
```
注：text里内容为字体图标代码，字体图标的颜色、大小设置同TextView一致
字体图标代码获取如下
![步骤11](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/11.png)
也可在下载的资源文件里中点击demo_index.html查看字体图标代码
![步骤12](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/12.png)
![步骤13](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/13.png)

附字体图标使用效果图如下
![步骤14](%E3%80%90Android%20%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6%E6%90%AD%E5%BB%BA%E3%80%91-%E4%BD%BF%E7%94%A8Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93/%E6%AD%A5%E9%AA%A4%E5%9B%BE%E7%89%87/14.png)

Demo源码
源码地址 [MiQingWang/AndroidIconTextView](https://github.com/MiQingWang/AndroidIconTextView)
