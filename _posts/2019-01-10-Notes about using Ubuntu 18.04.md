---
title: 'Notes about using Ubuntu 18.04'
date: 2019-01-10
permalink: /posts/2019/01/blog-post-1/
tags:
  - Ubuntu
categories:
  - English
---

These are some basic setting for newly installed Ubuntu.

**1.How to install Ubuntu 18.04 on Windows 10 system**

*In my case, I burned .iso file on USB disk.*  
>Problem 1:   
Always corrupted by Grub.

>Solution 1:   
Just use EasyBCD and install through NeoGrub.

**2.Install markdown editor**

*In my case, I use Haroopad*  
The process is straitforward, just download a .deb and install.
>Problem 1:   
libraries libgconf-2.so.4 warning.

>Solution 1:   
install libgconf using `sudo apt install libgconf2-4`

>Problem 2:   
Failed to load module "canberra-gtk-module".

>Solution 2:   
install using `sudo apt-get install libcanberra-gtk-module`

*I still don't understand why the first double click always open a new blank window?*

>**Update 2019-01-15**  
After a severe crash of Haroopad, I swithed to Remarkable as markdown editor, simply and stable.

**3.Install Google Chromium and Foxit pdf reader**

Install through Ubuntu Software Center.  
Download `.run` file from Foxit website, because Document Viewer looks really fuzzy.   
Use `cd` to the directorty of `.run` and carry out `chmod +x filename.run` and then execute `./filename.run` and enjoy.  
In case of uninstall, there is a uninstall directory, just `cd` into it and execute `./uninstall`  

**4. Install Pinyin input**

You could refer to [this blog](https://blog.csdn.net/qq_33159059/article/details/85019467) and [this website](https://blog.csdn.net/haeasringnar/article/details/81809040) for further referrence.