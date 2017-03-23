---
ID: 6426
post_title: RunAbove Sandbox
author: k0nsl
post_date: 2014-11-04 15:16:01
post_excerpt: ""
layout: post
permalink: https://k0nsl.org/blog/runabove-sandbox/
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
  - "223"
---
[caption title="RunAbove" url="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove01_k0nsl.png"]

A quick draft with results for my <a href="http://runabove.me/VYDM" title="RunAbove Cloud Sandbox" target="_blank">RunAbove Cloud Sandbox</a>. The description of the RunAbove service is as follows:

<blockquote><strong>For developer, by developers.</strong>
<a href="http://runabove.me/VYDM" title="RunAbove" target="_blank">RunAbove</a> has been created by the OVH Group. We want to change the way you look at Cloud Computing Services.

Based on a new vision of Cloud Computing Services, RunAbove is the first mono-slot provider in the world.
We focus on ensuring the best performance in terms of I/O, network throughput, CPU and RAM.
RunAbove aims to provide a cloud infrastructure powerful and transparent, for developers all over the world so they can focus on their work by relying on unshakable resources. 
Unshakable resources!
</blockquote>

RunAbove is a $10 million investment <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/wpml_good.gif' />

The 'Cloud Sandbox' instances have no SLA (last time I checked) but my experience since I signed up has been stable and the network has been good as well. I also have a Power8 instance, but have not had any time to play with it much - not yet!

[slider crop="yes" slide1="/blog/k1/uploads/2014/11/k0nsl-RunAbove-Power8.png" slide2="/blog/k1/uploads/2014/11/k0nsl-RunAbove-Power8_02.png" slide3="/blog/k1/uploads/2014/11/k0nsl-RunAbove-Power8_03.png"][/slider]

The RunAbove panel looks like this in "simple"-mode:
<a href="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Simple-Panel01_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Simple-Panel01_k0nsl-203x300.png" alt="RunAbove-Simple-Panel01_k0nsl" width="203" height="300" class="alignnone size-medium wp-image-6433" /></a>

Here are my initial results for the 'Cloud Sandbox' instance.

[divider]Specs[/divider]

[sourcecode language="plain"]
RAM: 4 GB
HDD: 60 GB
CPU Model: Intel Xeon E312xx (Sandy Bridge)
CPU Cores: 1
CPU Speed: 3699 MHz
CPU Cache: 4096 KB
[/sourcecode]

[divider]UnixBench[/divider]

[sourcecode language="plain"]
UnixBench (w/ all processors): 2111.6
UnixBench (w/ one processor): 2101.9
[/sourcecode]

[divider]IOPS[/divider]

[sourcecode language="plain"]
ioping -c 10
request=1 time=0.3 ms
request=2 time=0.3 ms
request=3 time=0.4 ms
request=4 time=0.3 ms
request=5 time=0.3 ms
request=6 time=0.4 ms
request=7 time=0.3 ms
request=8 time=0.4 ms
request=9 time=0.4 ms
request=10 time=0.4 ms

10 requests completed in 9004.4 ms, 2921 iops, 11.4 mb/s
[/sourcecode]

[divider]FIO[/divider]

[sourcecode language="plain"]
FIO random reads:
randomreads: (g=0): rw=randread, bs=4K-4K/4K-4K, ioengine=libaio, iodepth=64
fio-2.0.9
Starting 1 process
randomreads: Laying out IO file(s) (1 file(s) / 1024MB)

randomreads: (groupid=0, jobs=1): err= 0: pid=6772: Tue Nov  4 13:45:11 2014
  read : io=1024.3MB, bw=258970KB/s, iops=64742 , runt=  4050msec
  cpu          : usr=13.63%, sys=56.71%, ctx=8246, majf=0, minf=85
  IO depths    : 1=0.1%, 2=0.1%, 4=0.1%, 8=0.1%, 16=0.1%, 32=0.1%, &amp;gt;=64=100.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, &amp;gt;=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.1%, &amp;gt;=64=0.0%
     issued    : total=r=262207/w=0/d=0, short=r=0/w=0/d=0

Run status group 0 (all jobs):
   READ: io=1024.3MB, aggrb=258969KB/s, minb=258969KB/s, maxb=258969KB/s, mint=4050msec, maxt=4050msec

Disk stats (read/write):
  vda: ios=258939/0, merge=0/0, ticks=167744/0, in_queue=167596, util=97.07%
Done

FIO random writes:
randomwrites: (g=0): rw=randwrite, bs=4K-4K/4K-4K, ioengine=libaio, iodepth=64
fio-2.0.9
Starting 1 process

randomwrites: (groupid=0, jobs=1): err= 0: pid=6778: Tue Nov  4 13:45:48 2014
  write: io=1024.3MB, bw=29081KB/s, iops=7270 , runt= 36066msec
  cpu          : usr=1.91%, sys=10.87%, ctx=169674, majf=0, minf=19
  IO depths    : 1=0.1%, 2=0.1%, 4=0.1%, 8=0.1%, 16=0.1%, 32=0.1%, &amp;gt;=64=100.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, &amp;gt;=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.1%, &amp;gt;=64=0.0%
     issued    : total=r=0/w=262207/d=0, short=r=0/w=0/d=0

Run status group 0 (all jobs):
  WRITE: io=1024.3MB, aggrb=29080KB/s, minb=29080KB/s, maxb=29080KB/s, mint=36066msec, maxt=36066msec

Disk stats (read/write):
  vda: ios=0/261361, merge=0/28, ticks=0/2469688, in_queue=2471032, util=99.78%
Done
[/sourcecode]

[divider]Download Speed[/divider]

[sourcecode language="plain"]
Cachefly: 16.1 MB/s
Linode, Atlanta, GA, USA: 15.0 MB/s
Linode, Dallas, TX, USA: 12.0 MB/s
Linode, Tokyo, JP: 5.97 MB/s
Linode, London, UK: 83.9 MB/s
OVH, Paris, France: 62.5 MB/s
SmartDC, Rotterdam, Netherlands: 40.6 MB/s
Hetzner, Nuernberg, Germany: 17.2 MB/s
iiNet, Perth, WA, Australia: 742 KB/s
MammothVPS, Sydney, Australia: 432 KB/s
Leaseweb, Haarlem, NL: 51.4 MB/s
Leaseweb, Manassas, VA, USA: 8.39 MB/s
Softlayer, Singapore: 2.52 MB/s
Softlayer, Seattle, WA, USA: 9.44 MB/s
Softlayer, San Jose, CA, USA: 8.81 MB/s
Softlayer, Washington, DC, USA: 15.6 MB/s
[/sourcecode]

[divider]Colormedia Benchmark[/divider]

[sourcecode language="plain"]
Colormedia Benchmark Version 6.2 (with CPU Benchmark)
Webseite [1]: www.colormedia.co
Webseite [2]: www.ensky.eu

Allgemeine Informationen

Prozessor :  Intel Xeon E312xx (Sandy Bridge)
Prozessor-Kerne :  1
Taktfrequenz pro Kern:  3699.986 MHz
Arbeitsspeicher : 3968 MB
SWAP : 0 MB
Laufzeit :   4 days, 16:16,

Netzwerk Benchmark

Download Geschwindigkeit:  colormedia (DE):
Download Geschwindigkeit:  Edis (AT): 25.5MB/s
Download Geschwindigkeit:  Netcologne (DE): 41.2MB/s
Download Geschwindigkeit:  FSIT (CH): 60.5MB/s
Download Geschwindigkeit:  Softlayer (Hong Kong): 4.31MB/s

Festplatten Benchmark

I/O Performance [1]:  250 MB/s
I/O Performance [2]:  241 MB/s
I/O Performance [3]:  222 MB/s

CPU Benchmark

real    0m10.609s
user    0m10.557s
sys     0m0.016s

admin@with-jews-you-lose:~$
[/sourcecode]

[divider]PetaByet Benchmark[/divider]

<iframe src="https://www.petabyet.com/embed/2014-11-04-f4cc4d1efa03904a856bfec3b10073e6/?style=default" width="400" height="650" seamless></iframe>

[divider]Speedtest.net[/divider]

<a href="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Speedtest01_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Speedtest01_k0nsl.png" alt="RunAbove-Speedtest01_k0nsl" width="300" height="135" class="alignnone size-full wp-image-6434" /></a>

<a href="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Speedtest02_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Speedtest02_k0nsl.png" alt="RunAbove-Speedtest02_k0nsl" width="300" height="135" class="alignnone size-medium wp-image-6435" /></a>

<a href="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Speedtest03_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/11/RunAbove-Speedtest03_k0nsl.png" alt="RunAbove-Speedtest03_k0nsl" width="300" height="135" class="alignnone size-medium wp-image-6436" /></a>

[divider]The End[/divider]

That's it for now. As with any other provider, one must give it several months before reaching a conclusion. But if you wish to give <b><u><a href="http://runabove.me/VYDM" title="RunAbove" target="_blank">RunAbove</a></u></b> a test, go ahead. I have not been disappointed by anything so far!