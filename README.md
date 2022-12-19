## Automated_Dependency_Tracking

## Problem – The Context 
Technology evolves rapidly and products regularly release new versions to address
bugs/vulnerabilities and to add new features. As Nology client moves towards
the SaaS (Software as a Service) model, keeping up to date with new releases for
any dependencies we use is critical for us to deliver an enterprise-grade, ready-to-
use product continuously to our clients. And this is only one thing development teams need to think about! Clients requesting
features, responding to competitors’ developments, updating documentation and
support channels, and tackling technical debt are all part of the overall strategy for
maintaining and growing a successful product. <br/>

Third party libraries refer to bits of code which aren’t maintained by the product
developer directly but are required to implement certain features – for example, D3.js
is an open-source front-end visualisation library that allows for web-safe graphics to
be constructed easily by abstracting the process of wrangling the drawing of SVG
images away from developers. This leaves them free to focus on transforming the
data itself into a form that makes sense. This approach saves development time,
proves functionality via community testimonials, and decouples the drawing functions
to enable several graphics to be created with similarly little effort. <br/>

However, this approach means that a change to D3.js requires all code interfacing
with that library to be evaluated. Often, developers will attempt to use third-party
software with long-term support releases (LTS) to reduce the frequency of this
happening, but this option is not always available, and given so much to consider
when developing new features, fixing bugs, or responding to clients, dependency
checking is often quite a low priority task. 
How might we keep on top of third-party libraries to minimise the impact of updates
to our development teams? 

## Business Value – The Application 
As a large part of Nology client is based on the Splunk software platform, thier
developers often have little control over platform upgrades that could create risks
such as: 
1. breaking compatibility with other dependencies,  
2. requiring us to change our code to remove deprecated features,  
3. changing the behaviour between our development and production environments, and 
4. invalidating documentation previously written with version-specific screeenshots. 
5. Having a way to notify and alert developers whenever a dependency like
Splunk is updated with a new release or if a version-specific issue is identified by the community would help with planning out future releases by ensuring that these changes aren’t missed during planning. This enables developers to effectively estimate workloads and ensure that the product is continuously supported.  
 
## Business Value 
A centralised web application tool where developers can easily search through
release and patch notes for third-party packages/libraries would reduce the chance
of developing for the wrong platform version. A tool like this could also provide
comparison between current and released version for easy tracking and issue
identification, ensuring development goes smoothly. Ideally, such a tool could also
alert developers of new third-party releases, sending detailed reports of potential
impacts, reducing the amount of development time spent tracking third-party
releases and shortening response time for mitigating any issues from new versions. 

## Personas – the users 
I am a product developer working to maintain a product on the Splunk platform. This
means I need to make sure that if the platform is updated, I know where to change
the code and what documentation is affected to ensure the product remains
compliant with compatibility and security requirements. Is there a quick way to check
if any of my code or documentation relies on third party libraries which have been
updated since the last product release? <br/>

I want to be notified when packages and libraries I use are changed or updated.
 

## Scope: 
● I want to be notified when packages and libraries I use are changed or updated. <br/>
● I want to see what files in my codebase have been affected by any third-party release. <br/>
● I want to see patch notes that have been released since the last release version of my software.<br/>
● I want to compare third-party patch notes between versions. <br/> <br/> 
 

**Bonus Scope**: if you find your team gets through the basic requirements quickly. <br/>
● I want Teams bot notifications when there is a new third-party release that affects my code.<br/>
● I want to export a list of changes to libraries after a release date in via spreadsheet or pdf. <br/>
● I want to export these changes to Jira.<br/>
● I want to visually tag each change as a security fix for the third-party library, a new feature in the library, or a bugfix. <br/> 

## Recommended Tech Stack 
● Scraper - Python. <br/>
● React - Material UI. <br/>
● AWS Amplify front end hosting. <br/>
● AWS Lambda API Gateway for any Backend you want build (serverless API). <br/>
● AWS SNS for notifications. <br/>
