---
layout: post
title: 5 Open source SaaS starters
date: 2021-05-03 12:11:00 +0000
categories: OpenSource
seo:
  type: BlogPosting
  name: 4 Open-Source SaaS starters - Node.js, Python

---
# What's that?

Starting a SaaS business is never easy - and has lots of repeatable parts such as: authentication, billing, user management, and more. I love to focus on what matters, which is the core algorithm/business value behind my SaaS.

***

## The List

***

### [SaaS Python base application with Flask, Vue, Bootstrap, Webpack](https://github.com/CaravelKit/saas-base)

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

***

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

***

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

***

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

***

### Full Stack FastAPI and PostgreSQL - Base Project Generator

[https://github.com/tiangolo/full-stack-fastapi-postgresql](https://github.com/tiangolo/full-stack-fastapi-postgresql "https://github.com/tiangolo/full-stack-fastapi-postgresql")

![](https://github.com/tiangolo/full-stack-fastapi-postgresql/raw/master/img/docs.png)

## Features:

* Full **Docker** integration (Docker based).
* Docker Swarm Mode deployment.
* **Docker Compose** integration and optimization for local development.
* **Production ready** Python web server using Uvicorn and Gunicorn.
* Python [**FastAPI**](https://github.com/tiangolo/fastapi) backend:
  * **Fast**: Very high performance, on par with **NodeJS** and **Go** (thanks to Starlette and Pydantic).
  * **Intuitive**: Great editor support. Completion everywhere. Less time debugging.
  * **Easy**: Designed to be easy to use and learn. Less time reading docs.
  * **Short**: Minimize code duplication. Multiple features from each parameter declaration.
  * **Robust**: Get production-ready code. With automatic interactive documentation.
  * **Standards-based**: Based on (and fully compatible with) the open standards for APIs: [OpenAPI](https://github.com/OAI/OpenAPI-Specification) and [JSON Schema](http://json-schema.org/).
  * [**Many other features**](https://fastapi.tiangolo.com/features/) including automatic validation, serialization, interactive documentation, authentication with OAuth2 JWT tokens, etc.
* **Secure password** hashing by default.
* **JWT token** authentication.
* **SQLAlchemy** models (independent of Flask extensions, so they can be used with Celery workers directly).
* Basic starting models for users (modify and remove as you need).
* **Alembic** migrations.
* **CORS** (Cross Origin Resource Sharing).
* **Celery** worker that can import and use models and code from the rest of the backend selectively.
* REST backend tests based on **Pytest**, integrated with Docker, so you can test the full API interaction, independent on the database. As it runs in Docker, it can build a new data store from scratch each time (so you can use ElasticSearch, MongoDB, CouchDB, or whatever you want, and just test that the API works).
* Easy Python integration with **Jupyter Kernels** for remote or in-Docker development with extensions like Atom Hydrogen or Visual Studio Code Jupyter.
* **Vue** frontend:
  * Generated with Vue CLI.
  * **JWT Authentication** handling.
  * Login view.
  * After login, main dashboard view.
  * Main dashboard with user creation and edition.
  * Self user edition.
  * **Vuex**.
  * **Vue-router**.
  * **Vuetify** for beautiful material design components.
  * **TypeScript**.
  * Docker server based on **Nginx** (configured to play nicely with Vue-router).
  * Docker multi-stage building, so you don't need to save or commit compiled code.
  * Frontend tests ran at build time (can be disabled too).
  * Made as modular as possible, so it works out of the box, but you can re-generate with Vue CLI or create it as you need, and re-use what you want.
  * It's also easy to remove it if you have an API-only app, check the instructions in the generated `README.md`.
* **PGAdmin** for PostgreSQL database, you can modify it to use PHPMyAdmin and MySQL easily.
* **Flower** for Celery jobs monitoring.
* Load balancing between frontend and backend with **Traefik**, so you can have both under the same domain, separated by path, but served by different containers.
* Traefik integration, including Let's Encrypt **HTTPS** certificates automatic generation.
* GitLab **CI** (continuous integration), including frontend and backend testing.

### Dashboard

[https://github.com/userdashboard/dashboard](https://github.com/userdashboard/dashboard "https://github.com/userdashboard/dashboard")

Dashboard packages everything web apps need into reusable, modular software. It runs separately to your application so you have two web servers instead of one

## Features:

* single website or interface for your users
* Dashboard requires NodeJS
* Payment integration with Stripe
* User management
* Various hosting backends
* Localization