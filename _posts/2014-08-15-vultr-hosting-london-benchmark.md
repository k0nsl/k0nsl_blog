---
ID: 6306
post_title: 'Vultr Hosting: London Benchmark'
author: k0nsl
post_date: 2014-08-15 09:28:23
post_excerpt: ""
layout: post
permalink: >
  https://k0nsl.org/blog/vultr-hosting-london-benchmark/
published: true
ag_review_post:
  - 'No'
ag_review_place:
  - Top of Post
ag_slide_crop:
  - 'yes'
ag_auto_play:
  - 'yes'
ag_share_style:
  - none
ag_author_style:
  - avatar_box
post_views_count:
  - "222"
---
[caption title="Vultr Hosting" url="https://k0nsl.org/blog/k1/uploads/2014/08/vultr_hosting01_k0nsl.png"]

A quick and rudimentary benchmark of <a href="http://www.vultr.com/?ref=6803376" title="Vultr Cloud Hosting" target="_blank">Vultr Hosting's</a> London region/location. More as a personal note than anything -- could perhaps be useful for other people as well. I've had this particular VPS for almost two months and it has been up for 58 days so far.

I use this VPS specifically for IRCd, linked to my main node: <a href="https://talk.k0nsl.org" title="k0nsl’s IRC" target="_blank">irc.k0nsl.org</a>. That's about it.

Here's those rudimentary benchmarks. Enjoy! <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/evilgrin39.gif' />


[divider]VPS Specs[/divider]

CPU model :  Vultr Virtual CPU 2
Number of cores : 1
CPU frequency :  3392.144 MHz
Total amount of ram : 742 MB
Total amount of swap : 0 MB
System uptime :   58 days, 11:57

[divider]PetaByet Benchmark[/divider]

<iframe src="https://www.petabyet.com/embed/2014-08-15-f5e33ae32da1c28dd60bba175dcf3d92/?style=default" width="400" height="650" seamless></iframe>

[divider]ServerKite Benchmark[/divider]

<a href="https://k0nsl.org/blog/k1/uploads/2014/08/ServerKike01_k0ns.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/08/ServerKike01_k0ns-942x1024.png" alt="ServerKike01_k0ns" width="620" height="673" class="alignnone size-large wp-image-6310" /></a>

[divider]Obligatory "dd" test[/divider]

root@halcyon:~# dd if=/dev/zero of=vultr-io bs=64k count=16k conv=fdatasync && rm -fr vultr-io
16384+0 records in
16384+0 records out
1073741824 bytes (1.1 GB) copied, 2.29734 s, 467 MB/s

[divider]ioping test[/divider]

root@halcyon:~# ioping . -c 5
4.0 KiB from . (ext3 /dev/disk/by-uuid/9cd4a4f7-96a0-4745-b073-a8f955d7cca2): request=1 time=1.2 ms
4.0 KiB from . (ext3 /dev/disk/by-uuid/9cd4a4f7-96a0-4745-b073-a8f955d7cca2): request=2 time=305 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/9cd4a4f7-96a0-4745-b073-a8f955d7cca2): request=3 time=286 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/9cd4a4f7-96a0-4745-b073-a8f955d7cca2): request=4 time=344 us
4.0 KiB from . (ext3 /dev/disk/by-uuid/9cd4a4f7-96a0-4745-b073-a8f955d7cca2): request=5 time=329 us

--- . (ext3 /dev/disk/by-uuid/9cd4a4f7-96a0-4745-b073-a8f955d7cca2) ioping statistics ---
5 requests completed in 4.0 s, 2.0 k iops, 7.8 MiB/s
min/avg/max/mdev = 286 us / 498 us / 1.2 ms / 365 us

[divider]Speedtest.net Test[/divider]

<a href="https://k0nsl.org/blog/k1/uploads/2014/08/vultr-london-speedtest01_k0nsl.png"><img class="alignnone size-full wp-image-6307" src="https://k0nsl.org/blog/k1/uploads/2014/08/vultr-london-speedtest01_k0nsl.png" alt="vultr-london-speedtest01_k0nsl" width="300" height="135" /></a>

<a href="https://k0nsl.org/blog/k1/uploads/2014/08/vultr-london-speedtest02_k0nsl.png"><img class="alignnone size-large wp-image-6308" src="https://k0nsl.org/blog/k1/uploads/2014/08/vultr-london-speedtest02_k0nsl.png" alt="vultr-london-speedtest02_k0nsl" width="300" height="135" /></a>

[divider]Reference[/divider]

Vultr VPS, see: <a href="http://www.vultr.com/?ref=6803376" target="_blank">VULTR.com</a> (<a href="http://www.vultr.com/?ref=6803376" target="_blank">link</a>).

PetaByet: <a href="https://www.petabyet.com/" target="_blank">https://www.petabyet.com/</a>

ServerKite: <a href="http://serverkite.com/" target="_blank">http://serverkite.com/</a>