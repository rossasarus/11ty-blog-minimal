---
title: Why did I choose eleventy / netlify?
date: 2020-04-18
author: RossD
published: true
summary: How to not get stuck when deciding on a blogging platform (for software developers)
tags:
  - tech
  - platform
  - eleventy
---
This wouldn't be a tech blog without some obsessive navel-gazing, now would it? I doubt anyone really cares how this site is hosted, but just in case - here's my justification for choosing 11ty and netlify! I've been meaning to start a blog/portfolio site for almost two years now. I looked into all sort of jam stack solutions, thought about coding something up from scratch, and even considered just writing bare html. I didn't want to go with wordpress because that feels like a cop out (even though it is definitely the 2nd best option) 

Ultimately I chose eleventy hosted on netlify for a few reasons:
<!-- excerpt -->

# How to not get stuck when deciding on a blogging platform (for software developers)
{% asset_img 'decision_tree2.png' 'tech decision tree' %}

I've been meaning to start a blog/portfolio site for almost two years now. I looked into all sort of jam stack solutions, thought about coding something up from scratch, and even considered just writing bare html. I didn't want to go with wordpress because that feels like a cop out (even though it is definitely the 2nd best option) 

Ultimately I chose eleventy hosted on netlify for a few reasons:

- It is incredibly easy to start up. A few clicks and there is a demo site set up in netlify, and a repo created in your github.
- It stores all of the content in markdown files, so if I choose something else in the future the data is already in a readable format.
- It is super fast - wordpress is slow to load, slow to 
- Having a static site distributed via CDN makes me feel like there isn't much surface area to attack. With wordpress I always feel like I'm an inch away from having to wipe an rebuild a site due to some 0-day. Rebuilding eleventy from the repo is... just called a normal deploy.

There are admittedly some downsides:
- I haven't figured out the netlify CMS yet, so it's all manual markdown work. That fits in with my vision of having a site with really minimal styling, but it might not be for everyone.
- I'm sure that this won't be `the cool thing` in a few years (months?) and it might also stop working. This point was mostly negated by the markdown-based post approach because it makes it easy for me to take my content with me.
- I am pretty confident with wordpress setup and control, and trying to add functionality/plugins to eleventy looks to be harder and more limited. I accept this because I'm not sure what else I would really need, but it does slightly concern me.