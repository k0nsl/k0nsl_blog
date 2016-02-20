---
ID: 6401
post_title: Backupsy — a month later!
author: k0nsl
post_date: 2014-10-25 17:38:34
post_excerpt: ""
layout: post
permalink: >
  https://k0nsl.org/blog/backupsy-month-later/
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
  - "289"
---
[caption title="Backupsy CP" url="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-one-month-later01_k0nsl.png"]

I've been with Backupsy for about one month now, I started my service with them at 09/14/2014 and up until now everything has been functioning as expected; no issues. The recent emergency maintenance which subsequently meant moving the node to another rack meant nothing, it all seamlessly went past me without any hiccups.

The only thing which really matters to me is the network connectivity (which has been fine). I am using Syncthing <sup>[2]</sup> to syncronise backups across several machines.

Here are a few benchmarks to compare to my previous benchmark <sup>[1]</sup> over one month ago. If you are looking for a solid provider for backing up your data, you might want to give this company a try -- I'm not disappointed <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/001_wub.gif' />

[divider]Speedtest.net Benchmark[/divider]

<a href="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-speedtest-a-month-later01_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-speedtest-a-month-later01_k0nsl.png" alt="backupsy-speedtest-a-month-later01_k0nsl" width="300" height="135" class="alignnone size-full wp-image-6403" /></a>

<a href="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-speedtest-a-month-later02_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-speedtest-a-month-later02_k0nsl.png" alt="backupsy-speedtest-a-month-later02_k0nsl" width="300" height="135" class="alignnone size-medium wp-image-6404" /></a>

<a href="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-speedtest-a-month-later03_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-speedtest-a-month-later03_k0nsl.png" alt="backupsy-speedtest-a-month-later03_k0nsl" width="300" height="135" class="alignnone size-medium wp-image-6405" /></a>


[divider]Cachefly wget[/divider]

<strong>Screenshot:</strong>

<a href="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-cachefly-a-month-later01_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-cachefly-a-month-later01_k0nsl-300x50.png" alt="backupsy-cachefly-a-month-later01_k0nsl" width="300" height="50" class="alignnone size-medium wp-image-6406" /></a>

<strong>Raw text:</strong>

[sourcecode language="plain"]root@backup51:~# wget cachefly.cachefly.net/100mb.test -O /dev/urandom
--2014-10-25 12:00:41--  http://cachefly.cachefly.net/100mb.test
Resolving cachefly.cachefly.net (cachefly.cachefly.net)... 205.234.175.175
Connecting to cachefly.cachefly.net (cachefly.cachefly.net)|205.234.175.175|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 104857600 (100M) [application/octet-stream]
Saving to: `/dev/urandom'

100%[====================================================================================================&gt;] 104,857,600 50.7M/s   in 2.0s

2014-10-25 12:00:43 (50.7 MB/s) - `/dev/urandom' saved [104857600/104857600][/sourcecode]


[divider]Traceroute[/divider]

[sourcecode language="plain"]root@backup51:~# traceroute survivor.k0nsl.org
traceroute to survivor.k0nsl.org (209.141.38.163), 30 hops max, 60 byte packets
 1  162.213.193.65 (162.213.193.65)  1.641 ms  1.624 ms  2.609 ms
 2  r1-side-from-bc1.inceronetwork.com (192.211.63.5)  0.225 ms  0.234 ms  0.218 ms
 3  ae15.cr2.dfw1.us.as4436.gtt.net (198.47.104.73)  0.767 ms  0.755 ms  0.714 ms
 4  ae10-208.dal33.ip4.gtt.net (173.241.130.153)  0.723 ms  0.704 ms  0.710 ms
 5  xe-10-2-0.nyc39.ip4.gtt.net (89.149.181.197)  41.410 ms  41.386 ms  41.395 ms
 6  * * *
 7  * * *
 8  * * *
 9  node16.buyvm.net (205.185.112.116)  76.543 ms  75.906 ms  76.061 ms
10  * * *
11  * * *
12  * * *
13  * * *
14  * * *
15  * * *
16  * * *
17  * * *
18  * * *
19  * * *
20  * * *
21  * * *
22  * * *
23  * * *
24  * * *
25  * * *
26  * * *
27  * * *
28  * * *
29  * * *
30  * * *[/sourcecode]

[sourcecode language="plain"]root@backup51:~# traceroute pcloud.com
traceroute to pcloud.com (74.120.8.14), 30 hops max, 60 byte packets
 1  162.213.193.65 (162.213.193.65)  2.096 ms  2.088 ms  2.113 ms
 2  r1-side-from-bc1.inceronetwork.com (192.211.63.5)  0.242 ms  0.257 ms  0.249 ms
 3  ae0.er2.dfw2.us.above.net (208.185.52.201)  0.871 ms  0.866 ms  0.875 ms
 4  above-telia.dfw2.us.above.net (64.125.12.46)  0.800 ms  0.814 ms  0.807 ms
 5  62.115.9.102 (62.115.9.102)  172.141 ms  172.148 ms  172.145 ms
 6  api8.pcloud.com (74.120.8.14)  0.740 ms  0.610 ms  0.596 ms[/sourcecode]

[divider]dd test[/divider]

<strong>Screenshot:</strong>

<a href="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-dd-a-month-later01_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/10/backupsy-dd-a-month-later01_k0nsl-300x37.png" alt="backupsy-dd-a-month-later01_k0nsl" width="300" height="37" class="alignnone size-medium wp-image-6407" /></a>

<strong>Raw text:</strong>

[sourcecode language="plain"]root@backup51:~# dd if=/dev/zero of=test bs=16k count=8k conv=fdatasync &amp;&amp; rm -rf test
8192+0 records in
8192+0 records out
134217728 bytes (134 MB) copied, 0.350515 s, 383 MB/s[/sourcecode]

[divider]PetaByet Benchmark[/divider]

<iframe src="https://www.petabyet.com/embed/2014-10-25-22b8f0e536100012f47f50b908833b45/?style=default" width="400" height="650" seamless></iframe>

[divider]References[/divider]
<ol>
	<li><a href="https://k0nsl.org/blog/backupsy-basic-tests/">https://k0nsl.org/blog/backupsy-basic-tests/</a></li>
        <li>Open Source Continuous File Synchronization <a href="http://discourse.syncthing.net/" target="_blank">http://discourse.syncthing.net/</a></li>
        <li><a href="https://backupsy.com/aff.php?aff=327" title="Backupsy" target="_blank">Sign up with Backupsy! https://backupsy.com/aff.php?aff=327</a></li>
</ol>