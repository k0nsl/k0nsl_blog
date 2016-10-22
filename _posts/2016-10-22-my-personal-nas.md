---
ID: 7104
post_title: My personal NAS
author: k0nsl
post_date: 2016-10-22 21:24:33
post_excerpt: ""
layout: post
permalink: https://k0nsl.org/blog/my-personal-nas/
published: true
---
I built a personal NAS<sup><a href="#fn1" id="ref1">[1]</a></sup> solution back in November of 2015 and it is a "budget solution" mostly based on hardware I already had lying around here at home.

It consists of the following hardware:

<ul class="list-2">
<li><strong>CPU:</strong> Intel(R) Core(TM) i7-2600K CPU @ 3.40GHz</li>
<li><strong>Motherboard:</strong> ASUS P8B75-MLE</li>
<li><strong>Memory:</strong> 8GB Kingston HyperX</li>
<li><strong>Disks:</strong> 1 WD Red 2TB for the OS and 4 WD Red 2TB for my pools</li>
<li><strong>Cooling:</strong> Custom water cooling</li>
<li><strong>Case:</strong> Corsair C70
</ul>

That is practically it when it comes to the hardware powering my NAS. The custom water cooling is a overkill as it could have been cooled by a cheap heat sink coupled with a quiet fan...but what fun is that? <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/evilgrin39.gif' />
I also have one add-in PCIe SATA III controller card as the motherboard itself has very few SATA III ports, some cheap generic brand I bought via Ebay and which was made in China; it cost me €12.50 with shipping included in the price.

<img src="https://k0nsl.img-cdn.ru/blog/k1/uploads/2016/10/k0nsl-nas-motherboard01_k0nsl-300x225.jpg" alt="k0nsl-nas-motherboard01_k0nsl" width="300" height="225" class="alignnone size-medium wp-image-7113" />

As for the operating service. I was very unsure what to go with at the time of assembling the system. My friend bogeygoy suggested that I should use NAS4Free, as he was satisfied with it himself. However, I wanted to check out something entirely new which wasn't very widely used.
<a href="https://k0nsl.img-cdn.ru/blog/k1/uploads/2016/10/rockstor01_k0nsl.png"><img src="https://k0nsl.img-cdn.ru/blog/k1/uploads/2016/10/rockstor01_k0nsl-300x169.png" alt="rockstor01_k0nsl" width="300" height="169" class="alignnone size-medium wp-image-7115" /></a>
So, what did I pick? Well, it's called Rockstor<sup><a href="#fn2" id="ref2">[2]</a></sup> and it really was something very new at the time. The first public release was published in July 2015, so at the time I installed it one could say it wasn't a very widely used operating system.
I am running version 3.8-14.22 and I'm pulling new releases from their test channel rather than the stable one. Yes, I like to live on the edge. The test channel, or branch, features new releases every five days (if there is one available). The stable release channel once every month. My system runs on kernel 4.6.

<a href="https://k0nsl.img-cdn.ru/blog/k1/uploads/2016/10/rockstor02_k0nsl.png"><img src="https://k0nsl.img-cdn.ru/blog/k1/uploads/2016/10/rockstor02_k0nsl-300x169.png" alt="rockstor02_k0nsl" width="300" height="169" class="alignnone size-medium wp-image-7116" /></a>

The web interface of Rockstor has a rather pleasant design based on Bootstrap 3 with a wide variety of features. You can for example create customized storage pools and you can enable their so-called "Rock-on"-feature which is just a fancy front-end for Docker; this will allow you to install various applications such as Deluge, EmbyServer, GitLab, OwnCloud, Sickrage and many more.

<a href="https://k0nsl.img-cdn.ru/blog/k1/uploads/2016/10/rockstor03_k0nsl.png"><img src="https://k0nsl.img-cdn.ru/blog/k1/uploads/2016/10/rockstor03_k0nsl-300x169.png" alt="rockstor03_k0nsl" width="300" height="169" class="alignnone size-medium wp-image-7117" /></a>

Thanks to my water cooling solution the NAS itself is running both cool and quiet. The temperature inside of my house is 16 C and as of this moment the NAS is reporting these following readinga:
<pre>
[root@nas01 ~]# uptime && sensors
 23:18:52 up 29 days,  8:04,  3 users,  load average: 0.27, 0.20, 0.16
acpitz-virtual-0
Adapter: Virtual device
temp1:        +27.8°C  (crit = +99.0°C)
temp2:        +29.8°C  (crit = +99.0°C)

coretemp-isa-0000
Adapter: ISA adapter
Physical id 0:  +32.0°C  (high = +80.0°C, crit = +98.0°C)
Core 0:         +32.0°C  (high = +80.0°C, crit = +98.0°C)
Core 1:         +28.0°C  (high = +80.0°C, crit = +98.0°C)
Core 2:         +28.0°C  (high = +80.0°C, crit = +98.0°C)
Core 3:         +22.0°C  (high = +80.0°C, crit = +98.0°C)
</pre>

That's with just one fan on the absolute lowest RPM on the dual radiator.

I have to say, despite this being a so-called "curry solution" I'm satisfied with it. I have had zero issues to speak of, none that would warrant mentioning anyway! <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/icon_e_wink.gif' />

<div class="divider">
<h5><span>References</span></h5>
</div>
<p id="fn1" style="font-family: 'Open Sans', sans-serif; font-size: 8pt;"><a href="#ref1">[1]</a> A Network Attached Storage (NAS) device is a storage device connected to a network that allows storage and retrieval of data from a centralized location for authorized network users and heterogeneous clients. NAS devices are flexible and scale-out, meaning that as you need additional storage, you can add on to what you already have. A NAS is like having a private cloud right in your home. It’s faster, less expensive and provides all the benefits of a public cloud, giving you absolute control.</p>
<p id="fn2" style="font-family: 'Open Sans', sans-serif; font-size: 8pt;"><a href="#ref2">[2]</a> Rockstor is a Linux/BTRFS based Network Attached Storage (NAS) and private cloud solution. It is distributed as a CentOS flavored Linux operating system with a newer kernel and Rockstor application software bundled together to easily install a system and manage your data. You can find more information about Rockstor, <a href="http://rockstor.com/" target="_blank">here</a>.</p>