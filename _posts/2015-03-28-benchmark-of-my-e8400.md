---
ID: 6877
post_title: Benchmark of my E8400
author: k0nsl
post_date: 2015-03-28 05:42:07
post_excerpt: ""
layout: post
permalink: >
  https://k0nsl.org/blog/benchmark-of-my-e8400/
published: true
---
A benchmark of my overclocked E8400. You can read about the details of this system in <a href="https://k0nsl.org/blog/new-system-up-running/" title="New system up and running">this post</a>.

[divider]System Specs[/divider]

<table class="table table-bordered table-striped" style="width: 400px;">
     <tbody>
         <tr><td>RAM</td><td>8 GB</td></tr>
         <tr><td>HDD</td><td>1827 GB</td></tr>
         <tr><td>CPU Model</td><td>Intel(R) Core(TM)2 Duo CPU     E8400  @ 3.00GHz</td></tr>
         <tr><td>CPU Cores</td><td>2</td></tr>
         <tr><td>CPU Speed</td><td>4095 MHz</td></tr>
         <tr><td>CPU Cache</td><td>6144 KB</td></tr>
     </tbody>
   </table>

[divider]UnixBench[/divider]

<table class="table table-bordered table-striped" style="width: 400px;">
     <tbody><tr><td>UnixBench (w/ all processors)</td><td><strong>3102.4</strong></td></tr>
   
     <tr><td>UnixBench (w/ one processor)</td><td><strong>1810.6</strong></td></tr>
   </tbody></table>

Raw UnixBench Output:
[sourcecode language="plain"]

   #    #  #    #  #  #    #          #####   ######  #    #   ####   #    #
   #    #  ##   #  #   #  #           #    #  #       ##   #  #    #  #    #
   #    #  # #  #  #    ##            #####   #####   # #  #  #       ######
   #    #  #  # #  #    ##            #    #  #       #  # #  #       #    #
   #    #  #   ##  #   #  #           #    #  #       #   ##  #    #  #    #
    ####   #    #  #  #    #          #####   ######  #    #   ####   #    #

   Version 5.1.3                      Based on the Byte Magazine Unix Benchmark

   Multi-CPU version                  Version 5 revisions by Ian Smith,
                                      Sunnyvale, CA, USA
   January 13, 2011                   johantheghost at yahoo period com


1 x Dhrystone 2 using register variables  1 2 3 4 5 6 7 8 9 10

1 x Double-Precision Whetstone  1 2 3 4 5 6 7 8 9 10

1 x Execl Throughput  1 2 3

1 x File Copy 1024 bufsize 2000 maxblocks  1 2 3

1 x File Copy 256 bufsize 500 maxblocks  1 2 3

1 x File Copy 4096 bufsize 8000 maxblocks  1 2 3

1 x Pipe Throughput  1 2 3 4 5 6 7 8 9 10

1 x Pipe-based Context Switching  1 2 3 4 5 6 7 8 9 10

1 x Process Creation  1 2 3

1 x System Call Overhead  1 2 3 4 5 6 7 8 9 10

1 x Shell Scripts (1 concurrent)  1 2 3

1 x Shell Scripts (8 concurrent)  1 2 3

2 x Dhrystone 2 using register variables  1 2 3 4 5 6 7 8 9 10

2 x Double-Precision Whetstone  1 2 3 4 5 6 7 8 9 10

2 x Execl Throughput  1 2 3

2 x File Copy 1024 bufsize 2000 maxblocks  1 2 3

2 x File Copy 256 bufsize 500 maxblocks  1 2 3

2 x File Copy 4096 bufsize 8000 maxblocks  1 2 3

2 x Pipe Throughput  1 2 3 4 5 6 7 8 9 10

2 x Pipe-based Context Switching  1 2 3 4 5 6 7 8 9 10

2 x Process Creation  1 2 3

2 x System Call Overhead  1 2 3 4 5 6 7 8 9 10

2 x Shell Scripts (1 concurrent)  1 2 3

2 x Shell Scripts (8 concurrent)  1 2 3

========================================================================
   BYTE UNIX Benchmarks (Version 5.1.3)

   System: ******************
   OS: GNU/Linux -- 3.16.0-23-generic -- #31-Ubuntu SMP Tue Oct 21 17:56:17 UTC 2014
   Machine: x86_64 (x86_64)
   Language: en_US.utf8 (charmap=&quot;UTF-8&quot;, collate=&quot;UTF-8&quot;)
   CPU 0: Intel(R) Core(TM)2 Duo CPU E8400 @ 3.00GHz (8190.4 bogomips)
          Hyper-Threading, x86-64, MMX, Physical Address Ext, SYSENTER/SYSEXIT, SYSCALL/SYSRET, Intel virtualization
   CPU 1: Intel(R) Core(TM)2 Duo CPU E8400 @ 3.00GHz (8190.4 bogomips)
          Hyper-Threading, x86-64, MMX, Physical Address Ext, SYSENTER/SYSEXIT, SYSCALL/SYSRET, Intel virtualization
   05:03:04 up 16:24,  2 users,  load average: 0,08, 0,03, 0,07; runlevel 2

------------------------------------------------------------------------
Benchmark Run: lör mar 28 2015 05:03:04 - 05:31:19
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       35599357.4 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     4396.8 MWIPS (9.9 s, 7 samples)
Execl Throughput                               5815.1 lps   (29.7 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1084149.3 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          325084.0 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       1569251.8 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2201018.0 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 216706.5 lps   (10.0 s, 7 samples)
Process Creation                              15048.2 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  12466.3 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   2093.7 lpm   (60.0 s, 2 samples)
System Call Overhead                        3302619.6 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   35599357.4   3050.5
Double-Precision Whetstone                       55.0       4396.8    799.4
Execl Throughput                                 43.0       5815.1   1352.4
File Copy 1024 bufsize 2000 maxblocks          3960.0    1084149.3   2737.8
File Copy 256 bufsize 500 maxblocks            1655.0     325084.0   1964.3
File Copy 4096 bufsize 8000 maxblocks          5800.0    1569251.8   2705.6
Pipe Throughput                               12440.0    2201018.0   1769.3
Pipe-based Context Switching                   4000.0     216706.5    541.8
Process Creation                                126.0      15048.2   1194.3
Shell Scripts (1 concurrent)                     42.4      12466.3   2940.2
Shell Scripts (8 concurrent)                      6.0       2093.7   3489.5
System Call Overhead                          15000.0    3302619.6   2201.7
                                                                   ========
System Benchmarks Index Score                                        1810.6

------------------------------------------------------------------------
Benchmark Run: lör mar 28 2015 05:31:19 - 05:59:35
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables       71769344.1 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     8787.1 MWIPS (9.9 s, 7 samples)
Execl Throughput                              11915.9 lps   (29.9 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1661969.2 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          461886.4 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       2396072.3 KBps  (30.0 s, 2 samples)
Pipe Throughput                             4378722.8 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 661012.5 lps   (10.0 s, 7 samples)
Process Creation                              21568.2 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  15310.0 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   2473.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        6106059.3 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   71769344.1   6149.9
Double-Precision Whetstone                       55.0       8787.1   1597.7
Execl Throughput                                 43.0      11915.9   2771.1
File Copy 1024 bufsize 2000 maxblocks          3960.0    1661969.2   4196.9
File Copy 256 bufsize 500 maxblocks            1655.0     461886.4   2790.9
File Copy 4096 bufsize 8000 maxblocks          5800.0    2396072.3   4131.2
Pipe Throughput                               12440.0    4378722.8   3519.9
Pipe-based Context Switching                   4000.0     661012.5   1652.5
Process Creation                                126.0      21568.2   1711.8
Shell Scripts (1 concurrent)                     42.4      15310.0   3610.9
Shell Scripts (8 concurrent)                      6.0       2473.5   4122.6
System Call Overhead                          15000.0    6106059.3   4070.7
                                                                   ========
System Benchmarks Index Score                                        3102.4
[/sourcecode]

        <h2 class="section-separator-heading">IOPS</h2>
          <h4>I/O Pings</h4>
          <pre>ioping -c 10
request=1 time=0.5 ms
request=2 time=0.3 ms
request=3 time=0.3 ms
request=4 time=0.3 ms
request=5 time=0.3 ms
request=6 time=0.4 ms
request=7 time=0.5 ms
request=8 time=0.4 ms
request=9 time=0.2 ms
request=10 time=0.2 ms

10 requests completed in 9004.0 ms, 2944 iops, 11.5 mb/s</pre>

          <h4>I/O Seek Test (No Cache)</h4>
          <pre>ioping -RD
301 iops, 1.2 mb/s
min/avg/max/mdev = 0.2/3.3/24.3/3.4 ms</pre>

            <h4>I/O Reads - Sequential</h4>
            <pre>ioping -RL
389 iops, 97.2 mb/s
min/avg/max/mdev = 2.4/2.6/20.1/0.7 ms</pre>

            <h4>I/O Reads - Cached</h4>
            <pre>ioping -RC
825704 iops, 3225.4 mb/s
min/avg/max/mdev = 0.0/0.0/0.0/0.0 ms</pre>

        <h2 class="section-separator-heading">DD</h2>
          <pre>dd if=/dev/zero of=sb-io-test bs=1M count=1k conv=fdatasync
<strong>8.12977 s, 132 MB/s</strong></pre>
          <pre>dd if=/dev/zero of=sb-io-test bs=64k count=16k conv=fdatasync
<strong>6.7385 s, 159 MB/s</strong></pre>
          <pre>dd if=/dev/zero of=sb-io-test bs=1M count=1k oflag=dsync
<strong>62.4599 s, 17.2 MB/s</strong></pre>
          <pre>dd if=/dev/zero of=sb-io-test bs=64k count=16k oflag=dsync
<strong>812.793 s, 1.3 MB/s</strong></pre>

      <h2 class="section-separator-heading">FIO</h2>

      <table class="table table-bordered table-striped" style="width: 400px;">
        <tbody>
            <tr><td>Read IOPS</td><td>189.0</td></tr>
            <tr><td>Read Bandwidth</td><td>775 KB/second </td></tr>
            <tr><td>Write IOPS</td><td>312.0</td></tr>

            <tr><td>Write Bandwidth</td><td>1.2 MB/second </td></tr>

        </tbody>
      </table>
      <h5>Raw FIO Output</h5>
      <pre>FIO random reads:
randomreads: (g=0): rw=randread, bs=4K-4K/4K-4K, ioengine=libaio, iodepth=64
fio-2.0.9
Starting 1 process
randomreads: Laying out IO file(s) (1 file(s) / 1024MB)

randomreads: (groupid=0, jobs=1): err= 0: pid=23389: Sat Mar 28 04:12:39 2015
  read : io=1024.3MB, bw=775611 B/s, iops=189 , runt=1384713msec
  cpu          : usr=0.05%, sys=0.10%, ctx=262215, majf=0, minf=69
  IO depths    : 1=0.1%, 2=0.1%, 4=0.1%, 8=0.1%, 16=0.1%, 32=0.1%, &gt;=64=100.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, &gt;=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.1%, &gt;=64=0.0%
     issued    : total=r=262207/w=0/d=0, short=r=0/w=0/d=0

Run status group 0 (all jobs):
   READ: io=1024.3MB, aggrb=757KB/s, minb=757KB/s, maxb=757KB/s, mint=1384713msec, maxt=1384713msec

Disk stats (read/write):
    dm-1: ios=262207/969, merge=0/0, ticks=88589400/180240, in_queue=88784936, util=100.00%, aggrios=262207/1156, aggrmerge=0/0, aggrticks=88610716/180240, aggrin_queue=88790964, aggrutil=100.00%
    dm-0: ios=262207/1156, merge=0/0, ticks=88610716/180240, in_queue=88790964, util=100.00%, aggrios=262072/858, aggrmerge=135/298, aggrticks=88549156/120284, aggrin_queue=88669352, aggrutil=100.00%
  sda: ios=262072/858, merge=135/298, ticks=88549156/120284, in_queue=88669352, util=100.00%
Done

FIO random writes:
randomwrites: (g=0): rw=randwrite, bs=4K-4K/4K-4K, ioengine=libaio, iodepth=64
fio-2.0.9
Starting 1 process

randomwrites: (groupid=0, jobs=1): err= 0: pid=23416: Sat Mar 28 04:26:39 2015
  write: io=1024.3MB, bw=1249.8KB/s, iops=312 , runt=839687msec
  cpu          : usr=0.27%, sys=0.65%, ctx=513457, majf=0, minf=5
  IO depths    : 1=0.1%, 2=0.1%, 4=0.1%, 8=0.1%, 16=0.1%, 32=0.1%, &gt;=64=100.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, &gt;=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.1%, &gt;=64=0.0%
     issued    : total=r=0/w=262207/d=0, short=r=0/w=0/d=0

Run status group 0 (all jobs):
  WRITE: io=1024.3MB, aggrb=1249KB/s, minb=1249KB/s, maxb=1249KB/s, mint=839687msec, maxt=839687msec

Disk stats (read/write):
    dm-1: ios=0/263131, merge=0/0, ticks=0/53462156, in_queue=53468084, util=100.00%, aggrios=0/263298, aggrmerge=0/0, aggrticks=0/53469572, aggrin_queue=53469572, aggrutil=100.00%
    dm-0: ios=0/263298, merge=0/0, ticks=0/53469572, in_queue=53469572, util=100.00%, aggrios=0/262759, aggrmerge=0/539, aggrticks=0/53383720, aggrin_queue=53383696, aggrutil=100.00%
  sda: ios=0/262759, merge=0/539, ticks=0/53383720, in_queue=53383696, util=100.00%
Done</pre>

[divider]End[/divider]

As for what to do with the system...I'm still undecided. Another thing: I should have put this benchmark on <a href="https://benchmarks.k0nsl.org" title="k0nsl Benchmark's" target="_blank">benchmarks.k0nsl.org</a> as that is where it belongs, but seeing as I did all the other posts about the E8400 on this blog, I decided to put the benchmark here as well.
It's not the end of the world <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/icon_e_wink.gif' />