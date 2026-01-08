原则上E01 车机都可以用，吉利帝豪GL 20/21款没有问题（怎么使用甲壳虫自行百度）  
使用甲壳虫上传mtk-su， libmnl.so到sdcard目录下，  
然后使用运行一下命令就可以修复GPS时间问题，一般就能结局定位不准问题。  

cp /sdcard/mtk-su /data/local/tmp  
cd /data/local/tmp  
chmod 755 mtk-su  
./mtk-su  
mount -r -w -o remount -text4 /system  
mv /system/lib/libmnl.so /sdcard/libmnl2.so   
cp /sdcard/libmnl.so /system/lib  
cd /system/lib  
chmod 755 libmnl.so  
reboot  
