+ 回到底部	
	+ android:layout_alignParentBottom="true"
+ 添加轮廓、阴影
	+ outlineProvider="bounds"
+ android:paddingTop
	+ 指该控件内部内容距离该控件上边缘的边距 
+ 按钮点击 selector 事件
	+ 在layout里面的 id 设置为 xml文件
	+ 两种按钮的变化在drawable/xml 里：

	```
	//img_home_selector.xml
	
	<selector xmlns:android="http://schemas.android.com/apk/res/android">


    <item android:drawable="@drawable/ic_home_normal" android:state_focused="false" android:state_pressed="false" android:state_selected="false"/>
    <item android:drawable="@drawable/ic_home_selected" android:state_focused="false" android:state_pressed="false" android:state_selected="true"/>


    <item android:drawable="@drawable/ic_home_selected" android:state_focused="true" android:state_pressed="false" android:state_selected="false"/>
    <item android:drawable="@drawable/ic_home_selected" android:state_focused="true" android:state_pressed="false" android:state_selected="true"/>

    <item android:drawable="@drawable/ic_home_selected" android:state_pressed="true" android:state_selected="true"/>
    <item android:drawable="@drawable/ic_home_selected" android:state_pressed="true" />

</selector>
	```
	
+ LinearLayout中设置 style,将多次重复的地步布局书写在style中完成

```
//activity_main.xml

style="@style/tab_menu_item"
```

```
//style.xml

    <!--底部tab 样式-->
    <style name="tab_menu_item">
        <item name="android:layout_width">0dp</item>
        <item name="android:layout_weight">1</item>
        <item name="android:layout_height">match_parent</item>
        <item name="android:background">@color/colorPrimary</item>
        <item name="android:gravity">center</item>
        <item name="android:paddingTop">4dp</item>
        <item name="android:orientation">vertical</item>
    </style>

```


