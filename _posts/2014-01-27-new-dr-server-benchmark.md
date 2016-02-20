---
ID: 6075
post_title: New Dr.Server Benchmark
author: k0nsl
post_date: 2014-01-27 23:14:13
post_excerpt: ""
layout: post
permalink: >
  https://k0nsl.org/blog/new-dr-server-benchmark/
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
  - minimal
ag_author_style:
  - avatar_box
post_views_count:
  - "418"
---
[caption title="Dr.Server" url="https://k0nsl.org/blog/k1/uploads/2014/01/drserver07_k0nsl.jpg"]

Mr. Kolakovic was nice enough to let me beta test their new Xen PV based service from their "BlazingFast" product line. So here is my somewhat truncated test, I have only done the most pertinent tests that I can think of.
For real evaluation I'm running a Seafile instance on it, synchronized between three boxes.

First, here's a quick look:

<a href="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-glances01_k0nsl.jpg"><img class="alignnone size-large wp-image-6084" alt="drserver-glances01_k0nsl" src="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-glances01_k0nsl-1024x496.jpg" width="620" height="300" /></a>

[divider]VPS specs[/divider]
<table class="table table-bordered table-striped" style="width: 400px;">
<tbody>
<tr>
<td>CPU model :</td>
<td>Intel(R) Xeon(R) CPU E3-1240 v3 @ 3.40GHz</td>
</tr>
<tr>
<td>Number of cores :</td>
<td>2</td>
</tr>
<tr>
<td>CPU frequency :</td>
<td>3392.204 MHz</td>
</tr>
<tr>
<td>Total amount of ram :</td>
<td>242 MB</td>
</tr>
<tr>
<td>Total amount of swap :</td>
<td>255 MB</td>
</tr>
<tr>
<td>System uptime :</td>
<td>2 days</td>
</tr>
<tr>
<td>I/O Speed</td>
<td>649 MB/s</td>
</tr>
</tbody>
</table>

[divider]DD[/divider]

<div id="k0de">
dd if=/dev/zero of=sb-io-test bs=1M count=1k conv=fdatasync
1.05744 s, 1.0 GB/s
</div>

<div id="k0de">
dd if=/dev/zero of=sb-io-test bs=64k count=16k conv=fdatasync
1.08421 s, 990 MB/s
</div>

<div id="k0de">
dd if=/dev/zero of=sb-io-test bs=1M count=1k oflag=dsync
3.10701 s, 346 MB/s
</div>

<div id="k0de">
dd if=/dev/zero of=sb-io-test bs=64k count=16k oflag=dsync
16.1761 s, 66.4 MB/s
</div>

[divider]UnixBench[/divider]

<table class="table table-bordered table-striped" style="width: 400px;">
        <tbody>
            <tr><td>UnixBench (w/ all processors)</td><td>1656.5</td></tr>
            <tr><td>UnixBench (w/ one processor)</td><td>687.6</td></tr>
        </tbody>
</table>

[divider]Speedtest.net Speed Test[/divider]

<a href="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-new_beta03_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-new_beta03_k0nsl.png" alt="drserver-new_beta03_k0nsl" width="300" height="135" class="alignnone size-full wp-image-6080" /></a>

<a href="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-new_beta02_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-new_beta02_k0nsl.png" alt="drserver-new_beta02_k0nsl" width="300" height="135" class="alignnone size-large wp-image-6079" /></a>

<a href="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-new_beta01_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/01/drserver-new_beta01_k0nsl.png" alt="drserver-new_beta01_k0nsl" width="300" height="135" class="alignnone size-full wp-image-6078" /></a>

[divider]End[/divider]

That's it for now. I will continue evaluating the service by using Seafile (<a href="http://seafile.com/" target="_blank">http://seafile.com/</a>). If somebody has any ideas on what other benchmarks to run, please let me know in a comment.
If you're interested in Dr.Server and want to buy their service I can wholeheartedly recommend them -- because apart from this beta server I do have other services with them and they've been awesome in every respect so far! <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/icon_thumbup.gif' />

Check out Dr.Server:
<a href="http://knsl.net/28615" title="Dr.Server" target="_blank">www.drserver.net</a>.