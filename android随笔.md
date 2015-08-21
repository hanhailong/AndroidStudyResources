###1.通过签名文件获取签名命令
HailongHandeMacBook-Pro:Documents HanHailong$ keytool -list -v -keystore songa.jks
  其中songa.jks是签名文件

###2.计算ActionBar的高度
TypedValue tv = new TypedValue();
if (getTheme().resolveAttribute(android.R.attr.actionBarSize, tv, true))
{
    actionBarHeight = TypedValue.complexToDimensionPixelSize(tv.data,getResources().getDisplayMetrics());
}

2.通过adb命令获取某个app的包名
首先打开这个app，然后执行adb shell命令：adb shell dumpsys activity top，就可以列出当前的包名、Activity、View Hierarchy等信息，如图：
![截图](https://github.com/hanhailong/AndroidStudyResources/blob/master/screenshot/adb_shell_activity_top.png)

