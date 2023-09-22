生成签名:
keytool -genkey -v -keystore release-key.keystore -alias cordova-demo -keyalg RSA -keysize 2048 -validity 10000

打包命令：
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore release-key.keystore './app-release-unsigned.apk' cordova-demo

in D:\AppDEV\android-sdk-windows\build-tools\29.0.3\lib
java -jar apksigner.jar sign --ks .\release-key.keystore --out output.apk .\app-release-unsigned.apk (有效)

检查是否签名：
keytool -printcert -jarfile .\app-release-unsigned.apk


http://ios.zoopda.com/post/70427

https://blog.csdn.net/zm17671443092/article/details/132048234?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522169529793916800227434962%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=169529793916800227434962&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-4-132048234-null-null.142^v94^insert_down1&utm_term=Cordova%20%E6%89%93%E5%8C%85%E5%AE%89%E5%8D%93&spm=1018.2226.3001.4187

https://blog.csdn.net/summerking/article/details/125416453?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_utm_term~default-0-125416453-blog-119003815.235^v38^pc_relevant_sort&spm=1001.2101.3001.4242.1&utm_relevant_index=1