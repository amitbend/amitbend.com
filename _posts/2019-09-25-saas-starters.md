---
layout: post
title:  "4 Open source SaaS starters"
date:   2019-09-25 16:16:01 -0600
categories: OpenSource
seo:
    type: BlogPosting
    name: "4 Open-Source SaaS starters - Node.js, Python"
---


# What's that?

Starting a SaaS business is never easy - and has lots of repeatable parts such as: authentication, billing, user management and more.
I love to focus on what matters, which is the core algorithm/business value behind my SaaS.

*****


## The List


*****

### [SaaS Python base application with Flask, Vue, Bootstrap, Webpack](https://github.com/CaravelKit/saas-base)

![](https://camo.githubusercontent.com/af9a824546eade6f687340387b254a0079812585/68747470733a2f2f73616173696465612e696f2f7374617469632f696d616765732f6c6f67696e2e706e67)

## Features:
* User authentication
* Email authentication (with email confirmation)
* User registration, login, logout
* Simple user profile page
* Payment support
* Fully stripe integration (plans list is automatically generated from your Stripe account)
* User plans support
* Payments method support (only credit cards for now, by Stripe)
* Users can select a plan, change it, cancel, pause, resume
* User can see all the history of payment-related actions

*****

[SaaS Boilerplate - Node.js](https://github.com/async-labs/saas)

Build your own SaaS business with SaaS boilerplate. Productive stack: React, Material-UI, Next, MobX, WebSockets, Express, Node.js , Mongoose, MongoDB. Written with TypeScript

![SaaS](https://user-images.githubusercontent.com/26158226/61417514-2891dd00-a8ac-11e9-97d4-53944fe8f897.png)
## Features

* Server-side rendering for fast initial load and SEO.
* User authentication with Google, cookie, and session.
* Production-ready Express server with compression, parser, and helmet.
* Transactional emails (AWS SES): welcome, team invitation, and payment.
* Adding email addresses to newsletter lists (Mailchimp): new users, paying users.
* File upload, load, and deletion (AWS S3) with pre-signed request for: Posts, Team Profile, and User Profile.
* Team creation, Team Member invitation, and settings for Team and User.
### Opinionated architecture:
* keeping babel and webpack configurations under the hood,
* striving to minimize number of configurations,
* withAuth HOC to pass user prop and control user access to pages,
* withLayout HOC for shared layout and to pass additional data to pages,
withStore HOC, developer-friendly state management with MobX,
* server-side rendering with Material-UI,
* model-specific components in addition to common components.
* Universally-available environmental variables at runtime.
* Server-side environmental variables managed with dotenv.
* Browser-side environmental variables managed with Next.js and webpack's process.env substitution (see ./app/.env.blueprint).
* Custom logger (configure what not to print in production).
* Useful components for any web app: ActiveLink, AutoComplete, Confirm, Notifier, MenuWithLinks, and more.
* Analytics with Google Analytics.
### Docker CE Integration:
* spawn MongoDB database for development.
* stage service stack with lean container images.
### Production-ready, scalable architecture:
* app - user-facing web app with Next/Express server, responsible for rendering pages (either client-side or server-side). app sends requests via API methods and fetch to api server's Express routes.
* api - server-only web app with Express server, responsible for processing requests for internal and external APIs.
we prepared both apps for easy deployment to now by Zeit.
* Subscriptions with Stripe:
* subscribe/unsubscribe Team to plan,
* update card information,
* verified Stripe webhook for failed payment for subscription.

*****

[Reeve - Web application scaffolding for production environments - Node.js](https://github.com/peterjoseph/Reeve)
![Reeve](https://camo.githubusercontent.com/c00d4ecc25c22f3baff93f6cc100e5988d259a00/68747470733a2f2f692e696d6775722e636f6d2f633663596d536c2e706e67)


## Features:
* Express Server
* React
* Redux
* Server Configuration & Environment Store
* Webpack
* Redis
* MySQL Server
* SASS
* Bootstrap
* i18n Translation File Support
* React-Tooltips
* Dropdown Alerts
* AVA Test System
* JS Validation
* Google Analytics
* Subdomains
* Session Storage
* React Router
* User Authentication
* Error Reporting
* JSON Web Tokens
* Polyfills & IE Support
* Email Sending
* Sentry error logging
* Papertrail logging
* API Rate Limiting


*****

[DjaoDjin - Python,Django](https://github.com/djaodjin/djaoapp)

![DjaoDjin](https://djaodjin.com/static/img/og-image.png)

Accounts & billing workflows every SaaS needs
DjaoDjin builds the infrastructure, so you can focus on your product.

## Features
* Landing pages - Homepage, pricing
* Account profiles
* Billing - Stripe
* Dashboards 
* Access control policies
* Registrations
* Authentication
* Checkout
* Vue.js Frontend