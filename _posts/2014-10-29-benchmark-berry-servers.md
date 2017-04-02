---
ID: 6415
post_title: Benchmark of Berry Servers
author: k0nsl
post_date: 2014-10-29 21:19:52
post_excerpt: ""
layout: post
permalink: >
  https://k0nsl.org/blog/benchmark-berry-servers/
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
  - "180"
---
[caption title="Berry Servers" url="https://k0nsl.org/blog/k1/uploads/2014/10/berryservers02_k0nsl.png"]

Hi friends,

I reckon, most people who know the k0nsl, they also know I'm a sucker for new stuff, right? Well...not in a material sense, of course! I could care less for any material things. But back to <strong><em>"Berry Servers"</em></strong>: when they launched their VPS line I almost hit the order button instantly, at the prospect of getting a few more cheap IRC nodes + new nodes for DNS clustering, but I kept trying to resist it, telling myself I've no use for more...fruitless! I was only able to resist for one day before I finally ordered one. Yes, it was weak of me.
I am the first person to admit that <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/icon_lol.gif' />

Berry Servers offers very cheap yearly VPS Hosting in Phoenix, Arizona.

At any rate, I am currently testing their 'Blueberry'-plan -- which they upgraded to a "Dewberry" in the end (only the memory was upgraded, IIRC) <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/wpml_smile.gif' />

The brief introduction would be the following blob:
<blockquote><a href="https://berry.pw/clients/aff.php?aff=001" title="Berry Servers" target="_blank">Berry Servers</a> is owned and run by <a href="https://www.epidrive.com/clients/aff.php?aff=010" title="Epidrive Webhosting Solutions" target="_blank">Epidrive Webhosting Solutions</a>. Berry Servers' main goal is to provide reliable and affordable VPS servers. All our plans include best effort support and 99% uptime guarantee. Stocks are limited so get yours while you still can.</blockquote>

A few generic results are in order. I will update this with more replete information on Thursday or Friday, as I've got very little time for this right now..

[divider]PetaByet Benchmark[/divider]

<iframe src="https://www.petabyet.com/embed/2014-10-29-4ac3f9de822b9d83052493c77ad146f0/?style=primary" width="400" height="650" seamless></iframe>

[divider]Traceroute[/divider]

BuyVM:
[sourcecode language="plain"]
root@berry:~# traceroute survivor.k0nsl.org
traceroute to survivor.k0nsl.org (209.141.38.163), 30 hops max, 60 byte packets
 1  107.158.245.234 (107.158.245.234)  0.029 ms  0.008 ms  0.007 ms
 2  104.140.0.101 (104.140.0.101)  45.579 ms  45.574 ms  45.565 ms
 3  104.140.0.57 (104.140.0.57)  0.296 ms  0.339 ms  0.332 ms
 4  ae1-207.phx10.ip4.gtt.net (46.33.80.65)  0.370 ms  0.365 ms  0.402 ms
 5  xe-3-3-2.lax21.ip4.gtt.net (141.136.106.85)  34.581 ms xe-1-2-3.lax21.ip4.gtt.net (89.149.187.110)  11.294 ms  11.293 ms
 6  pni-as3257-1-lax2.staminus.net (69.197.1.66)  9.243 ms  9.241 ms  9.227 ms
 7  * * *
 8  * * *
 9  node16.buyvm.net (205.185.112.116)  19.621 ms  19.562 ms  19.460 ms
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
30  * * *
root@berry:~#
[/sourcecode]

The IP below is not mine, that's an abuser from <a href="http://www.vultr.com/?ref=6803376" title="Vultr VPS" target="_blank">Vultr</a>:
[sourcecode language="plain"]
root@berry:~# traceroute 108.61.155.154
traceroute to 108.61.155.154 (108.61.155.154), 30 hops max, 60 byte packets
 1  107.158.245.234 (107.158.245.234)  0.023 ms  0.005 ms  0.004 ms
 2  104.140.0.93 (104.140.0.93)  2.035 ms  2.032 ms  2.027 ms
 3  104.140.0.57 (104.140.0.57)  0.263 ms  0.308 ms  0.302 ms
 4  10ge16-6.core1.phx2.he.net (216.218.230.253)  3.035 ms  3.082 ms  3.120 ms
 5  10ge15-3.core1.dal1.he.net (184.105.222.78)  25.402 ms  20.299 ms  25.395 ms
 6  10ge12-6.core1.chi1.he.net (184.105.213.118)  47.994 ms  47.994 ms  47.987 ms
 7  100ge5-2.core1.nyc4.he.net (184.105.223.162)  58.819 ms  84.483 ms  58.859 ms
 8  10ge5-1.core1.nyc6.he.net (184.105.222.82)  72.520 ms  72.966 ms  72.735 ms
 9  nyiix.gi3-6.cr1.nyc1.choopa.net (198.32.160.157)  60.157 ms  72.669 ms  59.931 ms
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
30  * * *
root@berry:~#
[/sourcecode]

This IP is not mine either -- It's a Chinese abuser:
[sourcecode language="plain"]
root@berry:~# traceroute 103.24.229.4
traceroute to 103.24.229.4 (103.24.229.4), 30 hops max, 60 byte packets
 1  107.158.245.234 (107.158.245.234)  0.043 ms  0.006 ms  0.005 ms
 2  104.140.0.105 (104.140.0.105)  948.792 ms  948.790 ms  948.784 ms
 3  104.140.0.57 (104.140.0.57)  0.227 ms  0.263 ms  0.257 ms
 4  ae1-207.phx10.ip4.gtt.net (46.33.80.65)  0.369 ms  0.364 ms  0.357 ms
 5  xe-8-3-0.lax20.ip4.gtt.net (89.149.182.181)  11.201 ms  11.235 ms  11.230 ms
 6  219.158.33.49 (219.158.33.49)  122.842 ms  121.267 ms  121.303 ms
 7  219.158.102.177 (219.158.102.177)  299.051 ms  299.062 ms  299.057 ms
 8  219.158.19.201 (219.158.19.201)  304.397 ms  304.334 ms  304.384 ms
 9  219.158.96.229 (219.158.96.229)  273.640 ms  273.623 ms  273.664 ms
10  219.158.101.117 (219.158.101.117)  188.084 ms  186.340 ms  186.946 ms
11  219.158.8.186 (219.158.8.186)  207.012 ms  206.527 ms *
12  202.99.116.198 (202.99.116.198)  188.781 ms  189.053 ms  189.634 ms
13  117.8.1.186 (117.8.1.186)  258.497 ms *  258.658 ms
14  61.136.63.94 (61.136.63.94)  222.683 ms  223.167 ms  223.155 ms
15  103.24.229.4 (103.24.229.4)  254.300 ms  253.773 ms  255.354 ms
root@berry:~#
[/sourcecode]

Traceroute to INIZ:
[sourcecode language="plain"]
traceroute to 162.217.250.2 (162.217.250.2), 30 hops max, 60 byte packets
 1  107.158.245.234 (107.158.245.234)  0.039 ms  0.007 ms  0.006 ms
 2  * * *
 3  104.140.0.57 (104.140.0.57)  0.215 ms  0.260 ms  0.254 ms
 4  ae1-207.phx10.ip4.gtt.net (46.33.80.65)  0.338 ms  0.374 ms  0.321 ms
 5  xe-10-1-0.nyc20.ip4.gtt.net (89.149.184.226)  64.426 ms  64.471 ms  64.468 ms
 6  inforelay-gw.ip4.gtt.net (216.221.158.250)  64.543 ms  71.626 ms  71.613 ms
 7  cr1.lga2.inforelay.net (69.169.80.60)  61.331 ms  61.346 ms  61.385 ms
 8  cr1.lga2.ir.iniz.com (69.169.84.218)  62.114 ms  62.178 ms  62.223 ms
 9  nyc-vz1.iniz.com (162.220.240.2)  61.222 ms  61.091 ms  60.987 ms
10  nyc-us.lg.iniz.com (162.217.250.2)  61.798 ms  61.766 ms  61.998 ms
[/sourcecode]

[divider]Shoahbench[/divider]

[sourcecode language="plain"]

 ____  _                 _     _                     _
/ ___|| |__   ___   __ _| |__ | |__   ___ _ __   ___| |__
\___ \| '_ \ / _ \ / _` | '_ \| '_ \ / _ \ '_ \ / __| '_ \
 ___) | | | | (_) | (_| | | | | |_) |  __/ | | | (__| | | |
|____/|_| |_|\___/ \__,_|_| |_|_.__/ \___|_| |_|\___|_| |_|

Kommandant: root
----------------------------------------------------------------
Crematory :  Intel(R) Xeon(R) CPU E3-1231 v3 @ 3.40GHz
Furnace frequency :  3399.807 MHz
Cremation capacity : 128 MB
Number of muffles : 1
Baggage storage facilitation :  149 MB/s
Swampiness : 0
Country: Narnia
Interned for :   16:42,
----------------------------------------------------------------
Virtual cattle car speed from CacheFly: 78.3MB/s
Virtual cattle car speed from Coloat, Atlanta GA: 6.10MB/s
Virtual cattle car speed from Softlayer, Dallas, TX: 57.9MB/s
Virtual cattle car speed from Linode, Tokyo, JP: 13.7MB/s
Virtual cattle car speed from i3d.net, Rotterdam, NL: 8.26MB/s
Virtual cattle car speed from Leaseweb, Haarlem, NL: 839KB/s
Virtual cattle car speed from Softlayer, Singapore: 10.6MB/s
Virtual cattle car speed from Softlayer, Seattle, WA: 59.4MB/s
Virtual cattle car speed from Softlayer, San Jose, CA: 80.4MB/s
Virtual cattle car speed from Softlayer, Washington, DC: 30.2MB/s
Survival chance: 4681%
root@berry:~#
[/sourcecode]

[divider]Colormedia Benchmark[/divider]

[sourcecode language="plain"]
Colormedia Benchmark Version 6.2 (with CPU Benchmark)
Webseite [1]: www.colormedia.co
Webseite [2]: www.ensky.eu

Allgemeine Informationen

Prozessor :  Intel(R) Xeon(R) CPU E3-1231 v3 @ 3.40GHz
Prozessor-Kerne :  1
Taktfrequenz pro Kern:  3399.807 MHz
Arbeitsspeicher : 128 MB
SWAP : 0 MB
Laufzeit :   1 day, 1:44,

Netzwerk Benchmark

Download Geschwindigkeit:  colormedia (DE): 4.79MB/s
Download Geschwindigkeit:  Edis (AT): 742KB/s
Download Geschwindigkeit:  Netcologne (DE): 5.33MB/s
Download Geschwindigkeit:  FSIT (CH): 7.11MB/s
Download Geschwindigkeit:  Softlayer (Hong Kong): 12.7MB/s

Festplatten Benchmark

I/O Performance [1]:  157 MB/s
I/O Performance [2]:  161 MB/s
I/O Performance [3]:  162 MB/s

CPU Benchmark

real    0m9.607s
user    0m9.598s
sys     0m0.000s


root@berry:~#
[/sourcecode]

[divider]The End[/divider]

I'll run the <a href="http://quotes.k0nsl.org/shoahbench.html" target="_blank">"Shoahbench"</a> on it when I've done more tweaks to the script + more <small>[<strong>UPDATE:</strong> this has now been added, see above]</small>. Right now I'm going to sit back a few months to evaluate their offering. As I always do.
So far nothing out of the ordinary save for a mishap on launch. Not a big deal. They fixed it and my service is working fine so far.

You can give "Berry Servers" a try and see what you think of their service by <a href="https://berry.pw/clients/aff.php?aff=001" target="_blank"><u>clicking here</u></a>.

Adieu!