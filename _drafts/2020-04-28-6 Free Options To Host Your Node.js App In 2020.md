---
layout: post
title: 6 Options To Host Your Node.js App In 2022
date: 2022-08-01 21:00:00 +0000
categories: Node.js
seo:
  name: Six Options To Host Your Node.js App In 2022
  type: BlogPosting

---
### 6 Free Ways To Host Your Node.js App In 2022

![](/uploads/Free node.js hosting 2019.png)

\[Updated August 2022\]

So, you had a nice idea — you developed it, but now, you really don’t want to pay a monthly fee to a hosting provider. (And I totally understand you 😍) + corona crisis is just making you even cheaper.

I've updated the info for 2022 and added new free providers!

Don’t worry I’ve got your back! I listed here 6 of the best options with all the information you need — so let’s start!

***

![](https://cdn-images-1.medium.com/max/800/1*YxUHXJi_3k_hyBxmsu_HIA.png)

### #1 — Openshift (Red Hat)

**Highlights:**

* 2GB RAM, 2GB Persistent storage
* Unlimited network
* 1 Project per account
* Credit card — Not required
* Support — Community
* Considered secure

**Limitations/The Catch:**

* No custom domain
* Resource hibernation — Your project resources sleep after 30 minutes of inactivity, and must sleep 18 hours in a 72-hour period
* Expiration — Your subscription automatically expires after 60 days; resubscribe as often as you like

**Deployment:** Git (PaaS)

**Next tier cost**: Starts at $50/mo

**Most suitable for**: Small backend services, APIs, chatbots

[https://www.openshift.com/products/pricing/](https://www.openshift.com/products/pricing/ "https://www.openshift.com/products/pricing/")

![](https://firebase.google.com/images/social.png)

### #2 — Firebase functions

**Highlights:**

* Invocations - 125K/month
* GB-seconds - 40K/month
* CPU-seconds - 40K/month

**Limitations/The Catch:**

* Outbound networking - Google services only. quite problematic for many cases

**Deployment:** CLI

**Next tier cost**: Pay-as-you-go

**Most suitable for**: Small backend services, APIs

![Deta logo](https://docs.deta.sh/img/logo.svg)

### #3 — [Deta.sh]()

**Highlights:**

* 128 MB of RAM
* Running Nodejs 14.x by default
* Unlimited projects (!)
* Credit card — Not required
* Support — Community

**Limitations/The Catch:**

* Read-only file system. Only /tmp can be written to. It has a 512 MB storage limit - like a serverless function such as lambda
* HTTP Payload size limit is 5.5 MB.
* An execution times out after 10s

**Deployment:** CLI — NPM module (PAAS)

**Next tier cost**: space program - price is unknown

**Most suitable for**: Small backend services, APIs, chatbots, open-source projects

![](https://cdn-images-1.medium.com/max/800/1*YXdkLfCaVACGo-w_rx72KA.png)

### #4— Heroku

**Highlights:**

* 512mb RAM, No Persistent storage
* Unlimited network
* Custom domain support
* Credit card — Not required but your instance will have 550 hours a month (this mean it must sleep \~25% of the time), a verified account will give you 1000 hours a month (they will not charge you)
* Support — Business hour support, 1+ day response times

**Limitations/The Catch:**

* Sleeps after 30 mins of inactivity, otherwise always on depending on your remaining monthly free dyno hours. **tip -> **you can use a free ping service who will keep your service — I’m using [https://uptimerobot.com/](https://uptimerobot.com/ "https://uptimerobot.com/")

**Deployment:** CLI /Git (PAAS)

**Next tier cost**: Starts at $7 per month

**Most suitable for**: Fullstack project, or any type of small project

[https://www.heroku.com/pricing](https://www.heroku.com/pricing "https://www.heroku.com/pricing")

![now.sh](https://cdn-images-1.medium.com/max/800/1*31Y6x7fSKfdETiCjAORVbA.png "now.sh")

### #5 — Now.sh

**Highlights:**

* Serverless hosting!
* No limit for RAM, 100gb Persistent storage
* Network — up to 100 GB / mo
* Custom domain support
* Credit card — Not required
* Support —Community/Twitter
* Serverless invocations — 1,000 / day
* Maximum Execution Time- 10 seconds

**Limitations/The Catch:**

* Maximum File Size —  100mb
* Compared to 2020 the service is better much stabilized, but still might be bumpy

**Deployment:** CLI /Github integration/ Desktop app (PAAS)

**Next tier cost**: Starts at $0.99 per month

**Most suitable for**:

* Light compute Backend
* full-stack project

[https://zeit.co/pricing](https://zeit.co/pricing "https://zeit.co/pricing")

![glitch hosting free](https://cdn-images-1.medium.com/max/800/1*crKuSh8BTQdmVaD17hU1cQ.png "glitch hosting")

### #6— Glitch

**Highlights:**

* Glitch is a friendly community where everyone can discover and create the best stuff on the web — which means you can also host the app there!
* No limits specified, run on a container
* Unlimited Network
* Custom domain support
* Credit card — Not required

**Limitations/The Catch:**

* By default —  All code is open source, but you can change it to private for free
* 200MB disk space limit/ 512MB assets storage space.
* 512MB RAM
* For free users, Glitch apps go to sleep after five minutes of inactivity — if an app is waking up, your users might see a loading screen (we do this to keep our servers happy). Boosted apps don’t sleep and are always ready to go

**Deployment:** Github, Gitlab, Bitbucket (PAAS)

**Next tier cost**: 8$ monthly

**Most suitable for**: Pretty much everything open-source, you should try it

[https://glitch.com/pricing](https://glitch.com/pricing "https://glitch.com/pricing")