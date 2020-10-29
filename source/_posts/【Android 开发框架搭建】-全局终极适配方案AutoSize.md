## 前言

此方案为今日头条屏幕适配方案终极版，一个极低成本的 Android 屏幕适配方案，github star 10.7k受欢迎程度极高，侵入性非常低，该方案和项目完全解耦，在项目布局时不会依赖哪怕一行该方案的代码，而且使用的还是 Android 官方的 API。


## 项目介绍

该文章是根据AutoSize作者博客介绍总结记录，方便后续使用。
#### 官方中文介绍: [AndroidAutoSize-README-zh.md](https://github.com/JessYanCoding/AndroidAutoSize/blob/master/README-zh.md)
#### GitHub项目地址: [AndroidAutoSize](https://github.com/JessYanCoding/AndroidAutoSize)

<!-- more -->

## 原理

今日头条屏幕适配方案的核心原理在于，根据以下公式算出 density

##### 当前设备屏幕总宽度（单位为像素）/ 设计图总宽度（单位为 dp) = density
##### density 的意思就是 1 dp 占当前设备多少像素
##### 最终屏幕上显示的都是px大小所以px = dp * density，这样就能保证不同的屏幕上相同的##### dp不同的density得出的最终显示的px值达到适配效果。  

Android中的dp在渲染前会将dp转为px，计算公式：
##### px = density * dp;
##### density = dpi / 160;
##### px = dp * (dpi / 160);
##### 而dpi是根据屏幕真实的分辨率和尺寸来计算的，每个设备都可能不一样的。

## 使用

1.添加Gradle依赖

```java
  implementation 'me.jessyan:autosize:1.2.1'
```

2.在项目AndroidManifest 中填写全局设计图尺寸 (单位 dp)，如果使用副单位，则可以直接填写像素尺寸，不需要再将像素转化为 dp

```java
 <manifest>
    <application>            
        <meta-data
            android:name="design_width_in_dp"
            android:value="360"/>
        <meta-data
            android:name="design_height_in_dp"
            android:value="640"/>           
     </application>           
</manifest>
```

有两种类型的布局单位可以选择，一个是 主单位 (dp、sp)，一个是 副单位 (pt、in、mm)

主单位: 使用 dp、sp 为单位进行布局，侵入性最低，会影响其他三方库页面、三方库控件以及系统控件的布局效果，但 AndroidAutoSize 也通过这个特性，使用 ExternalAdaptManager 实现了在不修改三方库源码的情况下适配三方库的功能

副单位: 使用 pt、in、mm 为单位进行布局，侵入性高，对老项目的支持比较好，不会影响其他三方库页面、三方库控件以及系统控件的布局效果，可以彻底的屏蔽修改 density 所造成的所有未知和已知问题，但这样 AndroidAutoSize 也就无法对三方库进行适配

在使用主单位时，design_width_in_dp 和 design_height_in_dp 的单位必须是 dp，计算公式 dp = px / (DPI / 160) 将 px 尺寸转换为 dp 尺寸，如果实在找不到设备的 DPI 那就直接将 px 尺寸除以 3 或者 2 。

至此全局适配方案配置完成。  


3.如果使用副单位，需要在项目Application中添加以下初始化方法

```java
 AutoSizeConfig.getInstance().getUnitsManager()
        .setSupportDP(false)
        .setSupportSP(false)
        .setSupportSubunits(Subunits.MM);
```

## 高级使用方式

当某个 Activity 的设计图尺寸与在 AndroidManifest 中填写的全局设计图尺寸不同时，可以实现 CustomAdapt 接口扩展适配参数

1.Activity使用

```java
   public class CustomAdaptActivity extends AppCompatActivity implements CustomAdapt {

     /**
     * 是否按照宽度进行等比例适配 (为了保证在高宽比不同的屏幕上也能正常适配, 所以只能在宽度和高度之中选择一个作为基准进行适配)
     *
     * @return {@code true} 为按照宽度进行适配, {@code false} 为按照高度进行适配
     */
    @Override
    public boolean isBaseOnWidth() {
        return false;
    }

     /**
     * 设计图尺寸为 1080px * 1920px, 高换算成 dp 为 960 (1920px / 2 = 960dp)
     * <p>
     * 返回的设计尺寸, 单位 dp
     * {@link #getSizeInDp} 须配合 {@link #isBaseOnWidth()} 使用, 规则如下:
     * 如果 {@link #isBaseOnWidth()} 返回 {@code true}, {@link #getSizeInDp} 则应该返回设计图的总宽度
     * 如果 {@link #isBaseOnWidth()} 返回 {@code false}, {@link #getSizeInDp} 则应该返回设计图的总高度
     * 如果您不需要自定义设计图上的设计尺寸, 想继续使用在 AndroidManifest 中填写的设计图尺寸, {@link #getSizeInDp} 则返回 {@code 0}
     *
     * @return 单位 dp
     */
    @Override
    public float getSizeInDp() {
        return 667;
    }
  }
```

当某个 Activity 想放弃适配，请实现 CancelAdapt 接口

```java
  public class CancelAdaptActivity extends AppCompatActivity implements CancelAdapt {

  }
```

2.Fragment使用

首先在Application开启支持 Fragment 自定义参数的功能

```java
  AutoSizeConfig.getInstance().setCustomFragment(true);
```

当某个 Fragment 的设计图尺寸与在 AndroidManifest 中填写的全局设计图尺寸不同时，可以实现 CustomAdapt 接口扩展适配参数

```java
  public class CustomAdaptFragment extends Fragment implements CustomAdapt {

    @Override
    public boolean isBaseOnWidth() {
        return false;
    }

    @Override
    public float getSizeInDp() {
        return 667;
    }
  }
```

当某个 Fragment 想放弃适配，请实现 CancelAdapt 接口

```java
  public class CancelAdaptFragment extends Fragment implements CancelAdapt {

}
```

## 万能解决方案

在任何情况下本来适配正常的布局突然出现适配失效，适配异常等问题，只要重写 Activity 的 getResources() 方法即可，如果是 Dialog、PopupWindow 等控件出现适配失效或适配异常，同样在每次 show() 之前调用 AutoSize#autoConvertDensity() 即可。

```java
  @Override
  public Resources getResources() {
    //需要升级到 v1.1.2 及以上版本才能使用 AutoSizeCompat
    AutoSizeCompat.autoConvertDensityOfGlobal((super.getResources());//如果没有自定义需求用这个方法
    AutoSizeCompat.autoConvertDensity((super.getResources(), 667, false);//如果有自定义需求就用这个方法
    return super.getResources();
  }
```

## 总结

以上就是AutoSize的使用方式及介绍，如果需要使用自定义创建模拟设备预览图请参考文档顶部该框架作者的中文介绍，里面有详细的配置方式及框架的使用的方式。框架作者也提供demo-subunits源码来介绍项目中具体使用过程，这里我就不贴出项目的测试源码了，感谢观看，希望对你能有所帮助。
