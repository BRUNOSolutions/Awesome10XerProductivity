## Why curated AWESOME lists and RSS feeds matter so much

*We'd never keep up without curated reading lists that help us build RSS feeds ... especially in rapidly evolving industries with lots of investment driving R&D and new theoretical work.*

A rapidly developing research and development space such as eGPUs/eTPUs connectivity illustrates why. But, more generally, it is important to curate repositories of lists of AWESOME blogs and online publications by independent thinkerers, industry experts and research institutions ... by following these curated lists, or the abstracts from linked RSS feeds, one is better able to an eye on key things.  

So it's not JUST researchers/labs involved that developing as well as the conferences and workshops focused on HPC, cloud computing, and server technologies, as these often serve as a place for new ideas in cutting-edge research and development in eGPU/eTPU connectivity to emerge ... we ALSO continue to learn from [Archetypal Repository](https://github.com/sindresorhus/awesome) which laid the foundation for the broader archetypal example of listification in [the Awesome Lists of Awesome Lists](TheArchetype.md).

## Awesome Principles For Building a 10X-er Culture 

The outline of this curated list began as a [NewStack blog post](https://thenewstack.io/7-principles-and-10-tactics-to-make-you-a-10x-developer/).
 
### Principle 1: Speed

Developers are speed junkies. If they find a tool that’s 10 milliseconds faster, they would almost want to rewrite the entire application in it. But when it comes to how often they deploy code, they tend to be much more cautious. They would always rather deploy tomorrow, or next week so they don’t have to stay late today to fix whatever problems might happen.

When it comes to deployments, **speed increases safety** AND **small changes increase speed**.

Speed of shipping has massive compounding effects. If your deploy takes hours, you’re going to want to make dang sure there are no bugs, because if you find a critical bug right after a deployment goes live, then you have to wait another couple of hours for your fix to go live.

Aim for speed in every part of the software life cycle.

#### Faster feedback loops

#### Faster builds

#### Faster tests

#### Faster deployments

#### Faster fixes

#### Fast rollbacks

### Principle 2: Reliability

#### Your systems must be dependable.

Flaky CI/CD issues are one of the worst possible things in the universe.

Wring out the flakiness at every opportunity.

### Principle 3: Reproducibility

To build and maintain complex systems, we need to know that if we do X, we get Y, EVERY TIME on EVERY DEVELOPER's SYSTEM. If one time you do X, you get a Y, but then another time you get Z, all of the involved developers will lose ALL confidence in ALL of the systems that they need to be able to count on.

Use scripts and code to control everything you do instead of manual clicking, manual commands, etc.

### Principle 4: Calm On-Call Rotations

Calm on-call rotations are important because people can usually put up with stress during the workday, but if it creeps up in the rest of their life, that’s when they start updating their resumes.

If you don't get the need to CALM the workflow down ... another way to think of it that ***this is why we don't make busy people work all day and then drive three or four hours to a meeting at night so that they can drive three or four hours home to get a couple hours of sleep so that they can have no time with their families and go in tired/late to screw up their businesses.***  Is it any wonder that the political system has selected for PSYCHOTIC PEDO LUNATICS WHO BELONG IN PRISON rather than elected office.

### Principle 5: Easy to Debug

Everyone causes bugs. Even seniors, even when there is 100% test coverage. You will ship bugs to production, so you must be prepared to fix production bugs. If it’s hard to debug and slow to deploy fixes, it’s going to slow you down because you are going to add lengthy QA processes and before you know it, you’ll be deploying code only once every few weeks.

But even with lots of QA, you’ll still have production bugs. Production is the only tried-and-true way to find all the bugs. So our systems and code architectures must be easy to debug.

Review the whole software quality engineering body of knowledge ... where did CMMI come from? Look at how and why we aim for systems that are capable and mature.

### Principle 6: Self-Serve Infrastructure and Deployments

The old way of doing infrastructure and code deployments was you had two separate teams, devs and ops. If devs needed a new database, they would file a ticket with ops. If they needed a new service, file a ticket with ops. Need to deploy your code? File a ticket with ops.

This way led to devs often being blocked and waiting on ops to get to some ticket, devs not monitoring infrastructure stuff, and not getting feedback if their code was fast or slow, efficient or inefficient.

As an industry, we figured out it’s much better for devs to deploy and run their own code.

This is more efficient, they get stuck less, there is less communication overhead, and devs get more feedback from the real world on how their code is performing.

### Principle 7: Ship on Fridays

***Healthy*** engineering organizations deploy multiple times per day, including on Fridays.

If you are afraid to deploy on Fridays, it’s likely because:

You don’t have reliable deployments.
You have slow deployments.
You don’t have good monitoring and alerting.
Your app is hard to debug.
You don’t have tests.
Those are all things you must fix.

## AWESOME Practical 10X-er Cultural Practices

Suggestions ... maybe STRONG suggestions for things to aim for ... but not hard requirements ... at least not right away.

### Decouple Deployments from Releases
Fundamentally there are two possible actions for changing code in production: deployments and releases. Releasing refers to the process of changing user experience in a meaningful way. Deploying refers to the process of building, testing and rolling out changes to production software. The traditional process is that you change the code on a branch, and when it’s ready, you merge and deploy it. Once it’s deployed, users will see the new code.

But today’s modern engineering organizations use feature flags. What is a feature flag? It allows you to write new code alongside the old code, and then based on a runtime feature flag, your app decides to run the old or new code. This is huge.

Remember, speed is one of the key principles. Separating deployments from releases speeds up both because engineers can deploy their code as soon as it’s ready without waiting on product management to be ready to release it.

It also speeds up releases because now you can release a feature instantly. And roll back a feature instantly, without needing a deployment. Product managers can do releases on their own schedule.

Then even more advanced things are possible, like progressive rollouts, where you enable the feature flag for a percentage of your users. So, you could start out with 5% and if everything is working, then increase to 10%, 20%, etc. This is the best way to roll out changes because if there are problems, only a subset of your users will experience them, instead of all of them.

Feature flags are far superior to long-lived feature branches. You have fewer merge conflicts, less stale code, more team momentum, better team morale and more flexibility for testing things with real users.

### Continuous Deployment (CD)
Deployments are the heartbeat of an engineering organization. And just like a human heart, you want a steady rhythm of simple heartbeats. With this steady rhythm of deployments, you get momentum. And momentum is life for organizations.

And along with momentum, you get the efficiency of being able to deliver code to production as quickly as possible after it’s written.

You want to deploy as often as possible, multiple times per day. Every commit should be deployed. Small, understandable changes mean you have debuggable and understandable deployments.

The engineer who writes the code should merge their own pull request and then monitor production for any unexpected issues Feature flags, are a prerequisite for this, because they allow your team to ship small changes continuously instead of having long-lived feature branches.

### Set up and USE Notifications

Make sure you set up notifications for the following
• Failed builds

Failed deployments
Service downtime
Unhealthy servers
Unexpected errors
Unusual amount of traffic
Statuses of third-party services
⁃Many have a status page that you can subscribe to in Slack

The benefit is relatively obvious, but it does take at least a bit of effort to set them up, so this is something many teams can add as a quick win.

And if you already have notifications and alerts, you should audit them and ask these three questions:

Are they useful?
Are you getting too many false alerts so you ignore them?
Are there things you should add new alerts for?

### Optimize Deployment Speed
Your target for a happy team is 15 minute-or-less deployments.

Significantly longer than this is significantly painful. But significantly faster than this could take more work than it’s worth, depending on your circumstances.

There are several ways to improve your speed of deployment:

a. Track And Measure Your Current Deployment Times
You want to understand your starting point and which parts of the process are taking a long time. Those will be where you want to focus on improving.

b. Speed up Dependency Installation
This step is often one of the longest segments of deployment, so it can be a good first step.

Switch to pnpM if you’re using JavaScript. It’s a drop-in replacement for npm and Yarn that has significant performance and caching improvements
Cache the entire install step
Use your build system to totally cache this step, so this step doesn’t even run if your dependencies haven’t changed.

Example with Docker

 Zoom

Example with Nixpacks

 Zoom

c. Improve Your Build Speed
The main way to do this is to switch to a faster bundler.

If you are using create-react-app that uses webpack, you can switch to Vite which is way faster.

If using nextjs, upgrade to the latest and make sure you don’t have a .babelrc file. This will use SWC (Speedy Web Compiler) instead of Babel, which is a lot faster.

If you like living on the edge you can use Turbopack by passing the --turbo flag to next dev, but it’s only available for dev, not production builds yet.

d. Set up Build Caching
If you are using Docker, there are several things you can do.

Optimize your build layers. Use multistage builds. Set up remote caching.

Locally Docker caches by default and is fast, but in CI you don’t have a permanent machine. So you have to set up caching yourself. Refer to the Docker docs.

e.  Caching from the Future
If you want to really live with your hair on fire, in a good or a bad way, there is another style of caching that can give you some big wins, if you have a JavaScript project. Caching from the future works by having a single shared cache between your entire team and also CI.
This means if you build a commit locally and then push that commit to CI. The CI build will just download the cached build that you made and be done in mere seconds.

Or if someone else on your team already has built a commit, and then you run the build locally, it will again download the cache and be done in mere seconds instead of building from scratch again for you.

### Replace Staging with Preview Environments

Preview environments are temporary environments, typically tied to the life cycle of a pull request. When you open a pull request, infrastructure can be automatically provisioned for that PR.

This enables stakeholders to easily see the changes in a production-like environment. And then when the pull request is merged or closed, its environment will be automatically cleaned up.

They are a companion to feature flags. Larger changes should use feature flags and will often have many PRs for that feature. But small changes are often easier to re‐view with a preview environment instead of going through the hassle of managing a feature flag for it.

Preview environments are usually a better replacement for long-lived staging environments because staging is running all the time whether it needs to or not. And you have to merge a PR before anyone can verify the change.

### Infrastructure as Code
Hopefully you already have automated deployments, but you might not have automated infrastructure. Without Infrastructure as Code (IaC), you typically define your infrastructure configuration by clicking through a dashboard.

Bringing automation to your infrastructure configuration in the form of IaC has a huge number of benefits:

Repeatability / reproducibility
Consistency and standardization – predictability
Version controlled
Collaboration and review

### Platform Engineering
Back in the very old days, you had to rack your own servers in a data center. The abstraction level of infrastructure was extremely low. Then came Amazon Web Services (AWS) , which introduced cloud and raised the abstraction level. But it was still far too low for the average developer.

This led to the creation of Heroku, to the glee of developers all around the world. But that excitement was not to last, because ops were not happy. And it turns out abstractions like Heroku do not scale for large companies.

So ops takes over and tries a new thing between AWS and Heroku, IaC and Terraform. This works very well, but developers were not happy again.

Additionally, company leadership wants to increase operational efficiency, and one way to do that is provide devs with self-serve infrastructure, and so we started creating internal platforms that provide a better developer experience. Through that, the industry found a way for both ops and devs to be happy. And it has become known as platform engineering.

Now many companies are building some type of internal developer platform that can look more like an internal Heroku or more like just Terraform.

The three key concepts are:

It deploys to your own AWS/Google Cloud Platform (GCP) account.
Self-serve infrastructure with good developer experience.
Ops can dictate and customize the underlying primitives.Three of the main tools are Backstage, Humanitec and Flightcontrol.

### Work as Teams

Small team (two to six people, four is ideal)
Entire team works on one project at a time, together
Kickoff meeting (deep discussions on how to build)
Break project into small tasks (usually in kickoff)
Work on subtasks in parallel
Small PRs, at least one per day
Quick reviews / don’t be a blocker
Unblock yourself — merge your own safe PR if no one is available to review and you are blocked

### Trunk-Based Development For High Priority Code

For some distributed teams working on longer-term lower priority systems, issue-based development can work best -- because the developer will have other priorities ... but during sprints or at times when you are actually focused on getting stuff working, it probably best to get rid of pull requests, and commit straight to the main branch ... that's called trunk-based development.

Think of it like a cafeteria. Your tray is the main branch. When your burger is done, it goes on the tray. When the fries are ready, on the tray. When the milkshake is poured, tray. Once the tray is full, someone calls your number.

That’s how trunk-based development works. Every feature goes straight to main when it’s ready. Subtask or entire project doesn’t matter because they’re all fully working, independent and deployable.

If committing straight to main is too radical for you, then do the next best thing, which is short-lived branches. PRs shouldn’t last more than a day maximum. For a project, you should have many short PRs that are quick for others to review and are easy to merge. That’s how you get momentum.

### Eat Healthy and Exercise

We all need this reminder, being hunched over computers all day ... 25m FOCUS, then 4m TABATA HIIT ... focus/move every 30 minutes, all day. 

Make sure you take care of yourself ... try to take care of others -- *show you really CARE,* ie you already know how to do this, but if you need a reminder, listen to that old Dale Carnigie audiobook again.
