---
title: Fuck Disqus. 
date: 2021-06-09 18:06 +0001
excerpt_separator: <!--more-->
---

*The blog is being moved to blog.byemc.xyz, hosted on Tumblr.*

*This post contains Twitter embeds. Luckily, I spotted the `?refid=`s early and removed them from the links.*

Hello there! If you click on this post and take a look at the bottom of it, you should see a "Comments" section. And this morning, I discovered something horrible, something I never noticed because my default web browser ([Brave](//brave.com/)) has adblocking enabled by default. You ready to hear what it is? Disqus put ads on my website, without me knowing. (Spoiler, they're gone now)

<!--more-->

<blockquote class="twitter-tweet" data-dnt="true"><p lang="en" dir="ltr">Fuck you <a href="https://twitter.com/disqus">@disqus</a>. Actually. Fuck. You. You added ads to my comments, and I didn’t know about it until I checked a post on a browser without an ad blocker. Moving comment provider. I guess I shove looked carefully. <a href="https://t.co/Zo74VarHtB">pic.twitter.com/Zo74VarHtB</a></p>&mdash; ByeMC (@_ByeMC) <a href="https://twitter.com/_ByeMC/status/1402533505100300288">June 9, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

In short, I loaded up my website on my iPhone, looking at Safari through the iOS 15 beta. I tapped on my post and... what? What is this ad on my website!? I didn't put those there!
So I quickly searched up if Disqus used ads (the ads appeared above and below Disqus, but below the *Comments* header), and... yes. It does. 

Mad that I hadn't seen this sooner, I hastily plotted out this Tweet. And thought, *What would be a good replacement for Disqus?* So when I got home from school, I checked.

The theme used for this website is called [Minimal Mistakes](//mmistakes.github.io/minimal-mistakes/), and supports various comment providers. The comment providers it supports, is, according to the template `_config.yml`, [Disqus](//disqus.com/), [Discourse](//discourse.org/), [Facebook](https://developers.facebook.com/docs/plugins/comments), [Staticman, Staticman v2/v3](//staticman.net/) and [Utterances](https://utteranc.es/". Finding a suitable one, however, was a *bit* of a challenge.

I took a look at Discourse first, but was steered away by the $100 price tag. Dismissing Facebook (I assume you guys wouldn't want to sign up for accounts), I went to Staticman's website, only to not get my head around depolying it *without* giving away my card details. The last one remaining was... Utterances. And, I'm delighted to say it worked.

First, I installed [the app on my account](https://github.com/apps/utterances), and then going to [their website](//utteranc.es/) and filling in the form. When I got the info I needed, I extracted the info from the `<script>` tag they gave me. 

```html
<script src="https://utteranc.es/client.js"
        repo="[ENTER REPO HERE]"
        issue-term="pathname" <-- Get the info from here... -->
        theme="github-light" <-- ... and here -->
        crossorigin="anonymous"
        async>
</script>
```

I took the info marked above, and pasted it into `config.yml`, as the template already had these set up for me.

```yaml
  utterances:
    theme                : # "github-light" (default), "github-dark" - note I left it blank to fit the rest of the site.
    issue_term           : title # "pathname" (default)
```

No more ads, just GH Issues and your comments. Try it out below, with your GitHub accounts!

