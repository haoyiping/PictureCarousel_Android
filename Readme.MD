图片轮播控件CarouselerView
==========================
控件功能
--------------
+ **图片轮播展示**
+ **自动循环播放**
+ **横竖屏自动适配**

最新版本
-------
**v0.1 2016-1-7**

效果展示
--------
![控件实际效果](https://github.com/jingedawang/Resources/blob/master/recording.gif?raw=true)

起步
----
1. **从GitHub下载[源码](https://github.com/jingedawang/PictureCarousel_Android),下载的源码就是一个完整的工程，自带demo，可以直接运行看效果**

2. **拷贝以下文件到工程的相应位置**

    + `src/com/ucas/developer/picturecarousel_android/CarouselerView.java`
    + `src/com/ucas/developer/picturecarousel_android/CarouselException.java`
    + `src/com/ucas/developer/picturecarousel_android/ViewPagerAdapter.java`
    + `res/drawable-hdpi/dot.xml`
    + `res/drawable-hdpi/dark_dot.png`
    + `res/drawable-hdpi/white_dot.png`
    + `res/layout/carouseler.xml`
    + `libs/android-support-v4.jar`
    
3. **在你的Activity中使用该控件**

    在xml布局中直接使用本控件
    
        <com.ucas.developer.picturecarousel_android.CarouselerView
            android:id="@+id/carouseler"
    	    android:layout_width="match_parent"
    	    android:layout_height="match_parent" />
    
    并在Activity中获取到该控件
    
        carouselerView = (CarouselerView) findViewById(R.id.carouseler);
    
    然后为其设置图片资源，以四个图片为例
    
        ArrayList<Bitmap> bitmaps = new ArrayList<Bitmap>();
        bitmaps.add(BitmapFactory.decodeResource(getResources(), R.drawable.pic1));
        bitmaps.add(BitmapFactory.decodeResource(getResources(), R.drawable.pic2));
        bitmaps.add(BitmapFactory.decodeResource(getResources(), R.drawable.pic3));
        bitmaps.add(BitmapFactory.decodeResource(getResources(), R.drawable.pic4));
        carouselerView.setImageResources(bitmaps);
    
    之后可以选择性的设置是否开启或关闭自动播放，默认开启，若不想开启，只需调用如下方法传入参数false即可
    
        carouselerView.setAutoSlide(false);
        
4. **运行你的程序试试吧~**

文档
----
详细文档说明参见`doc/index.html`

作者信息
--------
**金戈大王**

邮箱：wjg172184@163.com<br>
新浪微博：[http://weibo.com/u/2503136032](http://weibo.com/u/2503136032)<br>
CSDN博客：[http://blog.csdn.net/u010829418](http://blog.csdn.net/u010829418)<br>
简书：[http://www.jianshu.com/users/8a84489c965c](http://www.jianshu.com/users/8a84489c965c)

欢迎来访交流~

其它版本
--------
[iOS版本](https://github.com/mingjiameng/LZP_PictureCarousel.git) 由[梁志鹏*-简书*](http://www.jianshu.com/users/d68767f43bf1/latest_articles)开发
