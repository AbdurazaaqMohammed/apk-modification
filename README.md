# apk-modification
Notes, tools, guides and more relating to modification of APK files

# Disclaimer
Please note that the information provided here is intended for educational and research purposes only. Always respect the rights of software developers and abide by the terms of service of the applications you modify.

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
<li>
 <a href="https://github.com/iBotPeaches/Apktool">Apktool</a> - A tool for reverse engineering Android APK files. It can decompile and recompile APKs, allowing you to modify the code and resources of an app. It is a command-line tool and requires Java to be installed on your system. Some of its features include:
<ul>
<li>Decoding and encoding of APK resources</li>
<li>Decompiling and recompiling APKs</li>
<li>Extracting and injecting resources</li>
<li>Debugging and analyzing APK files</li>
</ul>
</li>
<li>
 <a href="https://github.com/skylot/jadx">JADX</a> - Another tool for decompiling and analyzing Android APK files. It provides a graphical interface and allows you to browse the source code of an app. Some features of JADX include:
<ul>
<li>Decompiling and analyzing APK files</li>
<li>Browsing source code</li>
<li>Searching for specific classes or methods</li>
<li>Inspecting resources and assets</li>
<li>Exporting source code</li>
</ul>
</li>
 <li><a href="https://github.com/AbdurazaaqMohammed/AntiSplit-M"><strong>AntiSplit M</strong></a> - An open source app worked on by me to convert split APKs to a single APK.</li>
 <li><a href="https://github.com/AbdurazaaqMohammed/AXML-Editor"><strong>AXML Editor</strong></a> - Open source editor I worked on to edit Android binary XML files (AndroidManifest.xml and layout XML files).</li>
 <li><a href="https://github.com/AbdurazaaqMohammed/InjectDocumentsProvider"><strong>InjectDocumentsProvider</strong></a> - Access /Android/data and all data files of an Android app without any permissions by patching its APK file. This feature was created by Lin Jin Bin the developer of MT Manager but I created an open source app to inject it.</li>
<li><a href = "https://abdurazaaqmohammed.github.io/website/packageremovalhelper">Package Removal Helper</a> - a website tool to assist in the removal of packages (like trackers) from an APK by allowing input of the names of packages to be removed, and outputting a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions">regular expression</a></li>
