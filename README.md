# apk-modification
Notes, tools, guides and more relating to modification of APK files

# Disclaimer
Please note that this website is intended for educational and research purposes only. Always respect the rights of software developers and abide by the terms of service of the applications you modify.

# Introduction
This repository does not relate to "cracking" or "pirating" applications which is often associated with "Modded APKs", but rather several modifications and optimizations to APKs, mainly aiming to improve performance and reduce file size. This includes deletion of certain packages from APKs, such as analytics, crashlytics, trackers etc. This requires removing all invokes and reliances on the packages from the code of the APK.

# Tools
* [MT Manager](https://mt2.cn/download/) - Extremely useful file manager, designed with a major focus on APKs. A paid version is available, but the free version is sufficient for most necessary functions, and alternative tools are available for some. The official webite is in Chinese, the app is also uploaded [on APKCombo](https://apkcombo.com/mt-manager/bin.mt.plus/) by the developer, Lin Jin Bin. Useful features include:
  * Quick extraction of APKs
  * DEX file editor with features such as
    * Quick navigation between methods and classes
    * Quick search and replace in smali files, regex supported
    * Search strings in smali quickly
    * Quickly clear a method, also minimizing registers for optimization
    * Quickly clear all debug info (reduces size)
  * Minification of resources
  * Obfuscation of resources (this effectively saves space; but has a chance to break some apps)
  * Optimization of APKs
  * Automatically signing APKs after modification

* [Apktool M](https://maximoff.su/apktool/?lang=en) - Not to be confused with the Java program apktool, APKtool M is an app with many features, including
  * fast decompilation of APK files
  * Several optimizations for APKs. UltraZip is most effective; I have noticed it breaks media pickers in apps.
  * Antisplit - converting split .apks, .xapk, .apkm. files to .apk
  * integration with [MPatcher](https://maximoff.su/mpatcher/), another tool by the same developer, focusing on scripts to patch APKs in several ways, such as
    * optimizing images (it uses optipng and pngquant)
    * disabling (not removing) analytics
    * deleting languages except default language
    * deleting files that are unnecessary for the current device; this includes files for different CPU architectures or display sizes.
    * deleting some types of unused smali files
    * quickly separating APK with multiple to versions with individual libs to reduce size
    * support for writing custom scripts.

* [APK Editor](https://t.me/WSTprojects/1509) - A very old app, maintained by WSTprojects. Supports decompilation and custom patches, but is quite slow nowadays. It is still fast for quickly modifying XML files, which is a paid feature in MT Manager and requires fully decompiling in APKTool M.
