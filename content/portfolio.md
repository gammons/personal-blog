---
title: "Grant Ammons portfolio"
draft: false
---

[Download my resume](/assets/grant-ammons-resume.pdf)

#### Director of Engineering at ConvertKit

*Jan 2017 - Present*

[ConvertKit][ck] is an email marketing platform that focuses on creators.

* Scaled engineering org from **3 to 25+ engineers** (we're still hiring).  ConvertKit has [solid growth](https://convertkit.baremetrics.com/).  I joined when we were at around $6M in ARR, and I helped scale it to $24+M.
* Implemented many processes that were nascent or missing - hiring, software delivery, QA, reviews / promotions, etc. Helped ensure each process is effective.
* Scaled the team to squads, with squad leads.
* Migrated production infrastructure from Heroku to AWS.
* Helped set up teams to handle compliance + deliverability.
* Helped scale infrastructure to handle 1B+ email sends / month, as well as managing click, open, and delivery events in realtime.

#### PipelineDeals - VP engineering - 2006 to late 2016

[PipelineDeals][pld] is a SaaS CRM similar to close.io, Pipedrive, Salesforce, etc.

* Built [PipelineDeals][pld] with cofounders from idea to successful bootstrapped SaaS app generating millions in revenue.  Is employee #1.
* Hired and Managed 3 remote teams of awesome software engineers.
* [Ensured the culture is strong and vibrant](https://medium.com/@gammons/4-awesome-ways-to-level-up-your-dev-team-32ab43f90678#.z6bh97clv), even though team was remote.  Developer happiness and productivity were my primary concerns, while at the same time keeping accountability with the business side.
* [Crafted + continually honed][scrum] software delivery process to ensure high quality and tight collaboration.  Strived to keep process minimal.
* Managed a large production infrastructure in AWS, overseeing 50+ instances.  Implemented best-in-class practices to ensure speed, scalability, and uptime.   Achieved 99.999% uptime in 2015.  Kept infrastructure costs well below [SaaS averages][saas] by strategic use + planning of reserved instances.

---

#### Ultralist

![](/images/ultralist.png)

[Ultralist][ultralist] is an [open source](https://github.com/ultralist) command-line task management app written in Go.  It's my current side hustle focus.

**Utilizes the following tech:**

* Go - for the `ultralist` binary
* websockets for [realtime communication](https://github.com/ultralist/ultralist-websockets) between browser and binary
* Redis for websocket communication
* Rails api-only backend
* Mysql
* React via create-react-app for [the frontend](https://github.com/ultralist/ultralist-frontend)
* Progressive web app fundamentals
* material-ui for the CSS / interface
* Kubernetes for production + staging deployments
* Metabase for analytics

[Github repo for Ultralist](https://github.com/ultralist)

#### Ultradeck

![](/images/ultradeck.png)

Built my own SaaS, called Ultradeck.  Ultradeck was a developer-focused app to quicly create beautiful slides.

It did not get traction, but I learned a ton about product development.

While Ultradeck is no longer online, the [storybook](https://stories.ultradeck.co) still is.  The storybook gives you an idea of the breadth of the app.

I intend to open-source almost all of Ultradeck, starting with a [stripped-down version of the frontend](https://github.com/gammons/ultradeck-frontend) that communicates via a go-based binary to drive the slides.

**Utilized the following tech:**

* React via create-react-app
* Many custom markdown processing libraries
* Typescript
* Rails api-only backend
* Redis for websocket management / realtime
* Mysql


#### 12inch.reviews

![](/images/12inch.png)

[12inch.reviews](https://12inch.reviews) is a mash-up of [Pitchfork](https://pitchfork.com) reviews and [Spotify](https://spotify.com)'s web playback SDK, allowing you to quickly search for great music, and play it right on the website.

**Utilizes the following tech:**

* React
* Tailwind CSS
* Netlify lambda functions for access token management
* No backend!

[Github repo for 12inch.reviews](https://github.com/gammons/12inch.reviews)

#### demo-cli

![](/images/demo-cli.png)

Created a [simple library](https://demo-cli.dev) to show terminal-based demos in the browser.  Used in the marketing site for [Ultralist](https://ultralist.io).

[Github repo for demo-cli](https://github.com/gammons/demo-cli)

#### fake_arel

[fake_arel][fa] is a gem I wrote in 2010 that allowed developers to use Rails 3 query syntax in Rails 2.  It accomplished this by clever use of named scopes.

* We used this in production at PipelineDeals for a year or so while we refactored our app and readied it for Rails 3.
* Worked as advertised, as we were able to drop out fake_arel and begin using Rails 3 arel seamlessly.
* fake_arel was featured on the [Ruby5 podcast][r5] in 2010.

[Github repo for fake_arel](https://github.com/gammons/fake_arel)

[ck]: https://convertkit.com
[pld]: https://www.pipelinedeals.com
[ultralist]: https://ultralist.io
[saas]: http://www.forentrepreneurs.com/2015-saas-survey-part-2
[scrum]: https://medium.com/cto-school/ditching-scrum-for-kanban-the-best-decision-we-ve-made-as-a-team-cd1167014a6f#.u93fsg4qx
[fa]: https://github.com/gammons/fake_arel
[r5]: https://ruby5.codeschool.com/episodes/99-episode-97-july-27-2010
