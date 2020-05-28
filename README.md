
一款简洁实用的android广告栏，参考了[AndroidImageSlider](https://github.com/daimajia/AndroidImageSlider)和[BGABanner-Android](https://github.com/bingoogolapple/BGABanner-Android)结合自己的理解而成

### 导入
## Gradle Dependency
```
allprojects {
    repositories {
        ...
        maven { url "https://jitpack.io" }
    }
}

dependencies {
     compile 'com.github.dongjunkun:BannerLayout:1.0.6'
}

```

### 使用
**xml**
```
<com.yyydjk.library.BannerLayout
        android:id="@+id/banner"
        android:layout_width="match_parent"
        android:layout_height="200dp"
        app:autoPlayDuration="5000"
        app:indicatorMargin="10dp"
        app:indicatorPosition="rightBottom"
        app:indicatorShape="rect"
        app:indicatorSpace="3dp"
        app:scrollDuration="1100"
        app:selectedIndicatorColor="?attr/colorPrimary"
        app:selectedIndicatorHeight="6dp"
        app:selectedIndicatorWidth="6dp"
        app:unSelectedIndicatorColor="#99ffffff"
        app:unSelectedIndicatorHeight="6dp"
        app:unSelectedIndicatorWidth="6dp" />
```

**代码中使用**
```
//网络地址
bannerLayout.setViewUrls(urls);

//设置加载器
bannerLayout.setImageLoader(new GlideImageLoader());


//添加点击监听
bannerLayout.setOnBannerItemClickListener(new BannerLayout.OnBannerItemClickListener() {
            @Override
            public void onItemClick(int position) {
                Toast.makeText(MainActivity.this, String.valueOf(position), Toast.LENGTH_SHORT).show();
            }
        });
```
