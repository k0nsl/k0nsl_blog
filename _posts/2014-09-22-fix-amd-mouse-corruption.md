---
ID: 6356
post_title: Fix AMD Mouse Corruption
author: k0nsl
post_date: 2014-09-22 00:57:27
post_excerpt: ""
layout: post
permalink: >
  https://k0nsl.org/blog/fix-amd-mouse-corruption/
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
  - "125"
---
This is only a temporary fix for the dreaded "AMD Mouse Corruption"-issue, not a final solution by any means. If all the other solutions has failed, such as re-flashing your card with another BIOS, or whatever else you may have tried, then perhaps this will be of benefit for you. It's just a simple solution to a very annoying issue.

This is what I did to temporarily fix the issue while not gaming, because the mouse corruption appears in Windows as well, which complicates my work. Very irritating to say the least!

Enough jabber, here's how to get it (temporarily) resolved in Windows 8.1, but it should work the same way for most versions - just locate your device manager:

Press your Windows key + F and search for "Device Manager", or open it by pressing your Windows key + X to access the Power User Menu and locate "Device Manager" in the menu. But here is how I usually do it:
<a href="https://k0nsl.org/blog/k1/uploads/2014/09/fix-mouse-corruption01_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/09/fix-mouse-corruption01_k0nsl-300x246.png" alt="fix-mouse-corruption01_k0nsl" width="300" height="246" class="alignnone size-medium wp-image-6358" /></a>

Open it up and browse to "Display adapters" and click on the properties:
<a href="https://k0nsl.org/blog/k1/uploads/2014/09/fix-mouse-corruption02_k0nsl.png"><img src="https://k0nsl.org/blog/k1/uploads/2014/09/fix-mouse-corruption02_k0nsl-300x242.png" alt="fix-mouse-corruption02_k0nsl" width="300" height="242" class="alignnone size-medium wp-image-6359" /></a>

Click the "Driver"-tab and disable it. As you can tell, mine is already disabled. So whenever you wish to use it, just reverse the procedure and presto! You've got no more mouse corruption.

Another option is to use the iGPU if you're running Intel as I do, then just switch the HDMI cable to your motherboard - and voila! No more mouse corruption. A bit of a hassle, some may say, but in the end it's worth it because this issue is - as I say- very irritating and annoying. You'd think AMD would've fixed it by now. It's been a decade or something now, I forget, but they have not addressed the issue. At any rate, I know of no such fix from AMD and I've tried every damn solution out there and none of them work. The only ones that temporarily resolves it are the ones I have listed in this post.

That's it. Over and out <img class='wpml_ico' alt='' src='https://k0nsl.org/blog/k1/plugins/wp-monalisa/icons/icon_e_wink.gif' />