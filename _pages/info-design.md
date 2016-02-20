---
ID: 1892
post_title: Design Credits
author: k0nsl
post_date: 2012-11-11 21:55:27
post_excerpt: ""
layout: page
permalink: https://k0nsl.org/blog/info-design/
published: true
project10_post_views_count:
  - "31"
post_views_count:
  - "196"
metric-1-votes:
  - "2"
metric-1-score:
  - "0"
metric-2-votes:
  - "1"
metric-2-score:
  - "4"
---
<div class="et-box et-shadow">
<div class="et-box-content">
<p>This page is no longer relevant and/or contains out of date information.
</div></div>

This design is based on <a title="Asteroid" href="http://ronangelo.com/asteroid" target="_blank">Asteroid</a> by <a title="ronangelo" href="http://ronangelo.com/" target="_blank">ronangelo</a>. I intend to use this for the blog rather than the old design, which I didn't quite like.

I am still implementing the bits and pieces from my previous design into this one. I've already added all the shortcodes and my somewhat beefed up templating system so far. There's a problem with the design of the commentary bit and I have not investigated it further, but merely replaced it with the "About" box from my previous theme. I thought it fits quite nicely together with this design, although some minor changes probably has to be made.

When I hacked away the commentary bit (temporarily) I did it like so:
[sourcecode language="php"]
		&lt;!-- k0nsl_author_box --&gt;

   &lt;?php  if ( is_page('81') ): ?&gt;
        &lt;div id=&quot;respond&quot;&gt;&lt;p id=&quot;closed&quot;&gt;Prr, this part hasn't been dealt with. Yet.&lt;/p&gt;&lt;/div&gt;

    &lt;?php elseif ( is_page('136') ): ?&gt;
    &lt;div id=&quot;respond&quot;&gt;&lt;p id=&quot;closed&quot;&gt;Prr, this part hasn't been dealt with. Yet.&lt;/p&gt;&lt;/div&gt;
    &lt;?php elseif ( is_page('1745') ): ?&gt;
    &lt;div id=&quot;respond&quot;&gt;&lt;p id=&quot;closed&quot; align=&quot;center&quot;&gt;Forums hosted by &lt;a href=&quot;http://devnet-software.org&quot; target=&quot;_blank&quot;&gt;devNET software group&lt;/a&gt;&lt;/p&gt;&lt;/div&gt;
    &lt;?php elseif ( is_page('1469') ): ?&gt;
    &lt;div id=&quot;respond&quot;&gt;&lt;p id=&quot;closed&quot; align=&quot;center&quot;&gt;&lt;a href=&quot;http://devnet-software.org&quot; target=&quot;_blank&quot;&gt;devNET software group&lt;/a&gt;&lt;/p&gt;&lt;/div&gt;
    &lt;?php else: ?&gt;
		&lt;br&gt;
		&lt;div class='author-shortcodes'&gt;
			&lt;div class='author-inner'&gt;
		&lt;div class='author-image'&gt;
		&lt;img src='/static/k0nsl_57x57.jpg' alt='k0nsl' title=&quot;k0nsl&quot; /&gt;
			&lt;div class='author-overlay'&gt;&lt;/div&gt;
		&lt;/div&gt; &lt;!-- .author-image --&gt; 
		&lt;div class='author-info'&gt;
		&lt;h3&gt;&lt;?php _e(&quot;About k0nsl&quot;); ?&gt;&lt;/h3&gt;
			&lt;?php the_author_meta('description'); ?&gt;
		&lt;/div&gt; &lt;!-- .author-info --&gt;
			&lt;/div&gt; &lt;!-- .author-inner --&gt;
		&lt;/div&gt;
		&lt;!-- end k0nsl_author_box --&gt;
		
                &lt;!-- start: k0nsl_flatter --&gt;
                &lt;center&gt;
                &lt;a href=&quot;https://flattr.com/profile/k0nsl&quot; target=&quot;_blank&quot;&gt;
                &lt;img src=&quot;/static/flattr_k0nsl.png&quot; alt=&quot;Flattr this&quot; title=&quot;Flattr this&quot; border=&quot;0&quot; /&gt;&lt;/a&gt;
                &lt;/center&gt;
                &lt;!-- end: k0nsl_flatter --&gt;

	&lt;div id=&quot;comments-wrap&quot;&gt;
		&lt;h3&gt;React with a comment:&lt;/h3&gt;
		&lt;?php wp_list_comments( 'avatar_size=48' ); ?&gt;
		&lt;div class=&quot;pagination&quot;&gt;&lt;?php paginate_comments_links(); ?&gt;&lt;/div&gt;
	&lt;/div&gt;

     &lt;div id=&quot;comments-respond&quot;&gt;&lt;?php comment_form( 'comment_notes_before=&amp;comment_notes_after=' ); ?&gt;
                
    &lt;?php endif; ?&gt;
[/sourcecode]

Perhaps not the most glamorous way of doing it, but it works for me hehe.

[<strong>UPDATE:</strong> I've fixed so that the commentary bit works.]