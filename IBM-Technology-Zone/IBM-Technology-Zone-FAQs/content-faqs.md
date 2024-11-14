# Content FAQs

See below for frequently asked questions (FAQs) about content in Technology
Zone (TechZone).

## FAQ

### Is there a lifecycle for content in TechZone?

Yes. The content lifecycle contains the following steps:

1. Design
2. Create
3. Test
4. Publish
5. Support
6. Retire

#### Design

During the _design_ phase, you will first think about what the goals are for your TechZone
content.

* Is the content **already available** or **_mostly_ available**?
* What **product(s)** will the content showcase?
* What **use case(s)** does the content support?
* Is the content aligned with and **IBM [Sales Plays](https://ibm.seismic.com/Link/Content/DChBRcPbpmXf3GhDjTXBDJjMg49d)**?
* Is the content aligned with **IBM's [Well-Architected Framework](https://www.ibm.com/architectures/well-architected)**, and if it is not, is that clearly documented?
* On what **TechZone [Certified Base Image](https://techzone.ibm.com/collection/5fb3200cec8dd00017c57f20)** is the content based?
* Does your content require manual steps?
* How do you plan to **support** the content after it is published?

Before creating content, you should be able to answer all of these questions.

If content already exists in TechZone that solves _most_ of problems, consider contributing to that
content rather than creating your own. This is especially true with content that exists but includes
different versions of products that you need.  Consider contributing to the existing content to help
update it.

Pay attention to the product(s) that your content will showcase. Is there already TechZone content
that showcases the same product? Could it be adapted to your use case?

Does your content highlight a [use case](https://www.ibm.com/case-studies/search) that is currently
not highlighted by other TechZone content? Does your content fully-support the use-case, including
samples or examples or does your content stop at just installing the product and relying on the
content consumer to do the rest? Make sure you plan to install, configure, and initialize the
content with sample data to get the most out of demonstrating how the products support a use case.

Starting in 2024, to find content that supports IBM Sales Plays, publishing content will require
tagging the content with the relavent IBM Sales Play. If your content does not support any IBM Sales
Plays or is not aligned with the 2024 IBM strategy, you may re-consider creating, publishing, and
supporting the content.

#### Create

Creating your content requires you to develop automation or an automated process that **installs**,
**configures**, and **initialzes** your content.

The recommended new way to create content is to use OpenShift Pipelines to develop
pipelines to install, configure, and initialize on top of TechZone Certified Base
Images. This process is documented [here](#todo).

#### Test

Your content _must_ be tested and pass the tests before it can be published. You
should do your own testing and most likely will test many times while you are 
creating your content, but there are also automated tests that must complete
successfully before your content can be published.

#### Publish

Once you have your content created and tested, you are ready to publish your
content to TechZone. To publish your content, create a Collection in TechZone. You
can learn more about creating a Collection in the [TechZone Onboarding Collection](https://techzone.ibm.com/collection/onboarding).

#### Support

Creating and publishing your content are not the end of your content's life. 
You _must_ support your content, or it will be removed from TechZone. You must
supply a Slack channel that you will use to support your content, and the average
response time will be published as a badge on your content.

TechZone _only supports the Certified Base Images_. The TechZone team will not
support your content--that is up to you.

#### Retire

Like support, you must have a plan to retire your content. You may retire your
content for several reasons:

* The certified base images on which your content relies are now obsolete.
* The version of the product(s) in your content are obsolete.
* The use case your content highlights is no longer relavent.
* You no longer want to support your content.

Your content will be **retired for you automatically** if the following conditions
apply:

* You are not responsive to the Slack support channel.
* Your content fails automated testing.
* The certified base images on which your content relies are now obsolete.

There are no exceptions to this automated process.

### What are the expectations for author support in TechZone?

If you develop and publish content to TechZone, you are making a promise that you will keep the
content updated and support the content in a reasonable amount of time when or if people using
your content have issues with the content. As an author, you cannot publish content but expect
TechZone to support it for you.

Content must be updated at least once every 90 days. Content that is not updated every 90
days will automatically be set to "Draft" status and must be updated before you can publish it again.
Content in TechZone is audited with a continuous, automated process. To learn more about this, 
see [How is content in TechZone Audited?](#how-is-content-in-techzone-audited).

### How is content in TechZone audited?

Content in TechZone is audited by an automatic process that periodically scans
the content in TechZone for adherence to some rules. These rules are in the process
of being increased and improved so that TechZone can offer the highest-quality,
up-to-date content. Some examples of rules are:

1. Content must have been **updated within the last 90 days**.
1. Content must be used--content that is **unused** will automatically be archived.
1. Content must have **at least two collaborators**, in addition to the author.
1. Content text must **not include passwords or other credentials** information.
1. Content text must **not include email address** or other personal identifiable information (PII).

Other rules will be added and/or improved over time.

### Who supports the content in TechZone?

Broadly speaking, there content _authorship_ in TechZone is broadly seperated into two categories:

1. Content that is _authored_ by TechZone itself, and
2. Content that is _authored_ by contributors outside of TechZone (the "community").

TechZone is able to support the first type of content. In other words, if content is authored
and published by TechZone, you can expect help from TechZone directly when you open a ticket with
the TechZone helpdesk.

Content that is authored by contributors outside should be supported by the content author or
contributor. If the author or collaborators are unresponsive or unable to commit to supporting
the content, the content will be archived.

That means if you publish content to TechZone, you are responsible for supporting the content.
