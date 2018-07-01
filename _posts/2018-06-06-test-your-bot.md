---
layout: post
title:  "How to setup a comfortable Chatbot testing environment"
date:   2018-06-06 16:16:01 -0600
categories: Chatbots
seo:
    type: BlogPosting
    name: "How to setup a comfortable Chatbot testing environment"
---

# How to setup a comfortable Chatbot testing environment

I’m developing chatbots for some time, and testing them locally was always an
annoying part.



I also prefer not to download anything, and also not paying for any service



Let’s go through building a setup, with few simple steps:



1) **Create a testing bot profile** — It doesn’t matter which messaging platform
are you using — need to create a bot testing profile. for example for Facebook
Messenger you will need to create a new page,[ and also a new app connected to
this page.](https://developers.facebook.com/)



![](https://cdn-images-1.medium.com/max/800/1*xuPLz8rruHN3ZKZi0xxH6A.png)
<span class="figcaption_hack">Create a testing bot profile</span>



2) **use **[serveo.net](http://serveo.net/)** for tunneling** — there are plenty
of tunneling solutions you can use, where most of them cost a monthly.<br> We
are looking are looking for service which is:

* Free (because we are cheap 🙂)
* Support sub-domains (it’s extremely annoying to change the URL every time you
have to restart your computer)
* Robust (so you won’t have to reconnect every moment)
* No need to download (a Bonus!)

I tried *localtunnel* (free, not so robust), *ngrok* (no sub-domains on free
version) and few other. the winner is [serveo.net](http://serveo.net/)** **as it
answers all of my requirements (free, no download, support sub-domains)


example usage will be:

    ssh -R 
    80:localhost:8888 serveo.net

where you should run it the first time **without** a requested subdomain -> get
one from the server -> use it from now on.


<span class="figcaption_hack">Tunneling</span>

2) **make it even more robust — **My internet connection tends to be fragile,
and tunneling services tends to disconnect.

I looked for a simple service that will keep the ssh connection to *serveo*
alive & reconnect upon disconnection.

I’ve found [AutoSSH](http://www.harding.motd.ca/autossh/) which does all that, a
simple usage will be:


In our case will just need to change the ssh command of serveo to autossh (after
installing of course)

    autossh -R 
    80:localhost:8888 serveo.net

<span class="figcaption_hack">AutoSSH</span>

This is it! Happy testing.