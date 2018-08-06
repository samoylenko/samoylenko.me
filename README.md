[![Build Status](https://travis-ci.org/samoylenko/appseclearning.svg?branch=master)](https://travis-ci.org/samoylenko/appseclearning)

# Learning Application Security (quick path)

We created this project to share notes from our discussions about what would be
the the quickest path for someone who is just starting their career, to gain the
minimal knowledge and experience required to become a successful application
security specialist.

## What to learn (and why)

Becoming an application security professional requires knowledge and practice in
computer security and software development. This section is our recommendations
on how to start in these two areas.

We will focus mostly on the security part for two reasons: it's the primary
motivation for this document, and software development communities have already
created and published excellent guides on every topic of your choosing.

### Security skills

In the context of this document, security skills is the easiest part to start
learning with. Application security professional does not need to have very deep
knowledge of networks and operating systems security to start their career. We
focus only on the
[Application layer](https://en.wikipedia.org/wiki/OSI_model#Layer_7:_Application_Layer),
just one out of seven layers of the
[OSI model](https://en.wikipedia.org/wiki/OSI_model). But please note that items
like '_ensuring secrets are only transmitted over HTTPS_', or '_production
configuration files are protected at filesystem level_', are also part of the
application security domain.

#### "5+5" formula

We have a so-called "5+5" formula - you only need to read around 5 security
books and get familiar with around 5 security-related resources to obtain the
required security knowledge to start. Think about it - will take only around 3
months if you spend as little as 1-2 hours a day reading. And it will be quite
an interesting and motivational read which will also give you a good
understanding of what to look for when you will be exploring the software
development domain.

Below are our recommendation on where to start learning.

#### Theory

##### Books

1.  [CISSP CBK (Common Body of Knowledge)](https://www.isc2.org/Certifications/CISSP)

A great book by [(ISC)<sup>2</sup>](https://www.isc2.org) which not only
contains everything that security professional should know, but also provides a
good direction on how to apply your skills and bring value to people or
organizations you will work with.

2.  [CSSLP CBK](https://www.isc2.org/Certifications/CSSLP)

Another CBK by (ISC)<sup>2</sup> focused on software lifecycle.

We of course recommend reading both the CISSP and CSSLP CBKs (or, even better,
become (ISC)<sup>2</sup> member and get certified), but if you really have to
chose between the two, we recommend CISSP - it will give you a wider perspective
on security topics to start with.

3.  [Agile Application Security: Enabling Security in a Continuous Delivery Pipeline](http://shop.oreilly.com/product/0636920045106.do)

A long-awaited book that helps understand how security can be applied to the
modern world of agile software development.

4.  [The Web Application Hacker's Handbook: Finding and Exploiting Security Flaws](https://www.wiley.com/en-us/The+Web+Application+Hacker%27s+Handbook%3A+Finding+and+Exploiting+Security+Flaws%2C+2nd+Edition-p-9781118026472)

Some great penetration testers we met call this book their Bible of hacking and
keep it at their desk at all times.

5.  [The Tangled Web: A Guide to Securing Modern Web Applications](https://nostarch.com/tangledweb)

A great book on web application security recommended by many security
professionals.

##### Resources

1.  [OWASP TOP-10](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project)

The top common application security vulnerabilities list. You will often see that
for many of our colleagues, application security starts and
ends here. However, this list is just the beginning.

2.  [MITRE CWE (Common Weaknesses Enumeration)](https://cwe.mitre.org)

Knowledge base on security weaknesses. Vulnerabilities that are found
by security researchers are commonly mapped against CWE IDs - this is
a practice that we recommend to ensure having a common ground with all
parties involved in the vulnerability resolution process.

3.  [OWASP ASVS (Application Security Verification Standard)](https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project)

Great guide on what and how to look for in applications.

4.  [Hypertext Transfer Protocol Version 2 (HTTP/2)](https://tools.ietf.org/html/rfc7540)

HTTP is the protocol web applications use to communicate. Knowledge of
this protocol is essential for every application security professional.

##### Continuous learning

###### Podcasts

Listening to podcasts is a great way to stay on top of any updates in the
world of information security. We recommend
[**Security Weekly**](https://securityweekly.com/shows) shows - really great guys
who now have grown their original podcast, "Paul's Security Weekly", into a
number of shows covering different topics, and we recommend subscribing to all
of them. Lots of extremely useful info and fun. Absolutely not boring and very
motivational. Authors of this document are highly influenced by the Security
Weekly Crew and their shows.

#### Practice

1.  Complete these challenges to see common vulnerabilities in action:

    1.  [OWASP WebGoat](https://github.com/WebGoat/WebGoat)

    WebGoat has great tutorials and will guide you through everything.
    Its development version also teaches you how to fix common
    vulnerabilities in Java Web Applications. Additional lessons are
    available at [GitHub](https://github.com/WebGoat/WebGoat-Lessons).

    2.  [OWASP JuiceShop](https://github.com/bkimminich/juice-shop)

    JuiceShop is a good example of modern 'single-page'
    application, and it's challenges are fun!

2.  Learn to use attack proxies, these tools will help you see all communication
    aspects of web applications, learn how they interact and how parameters are
    being passed. This will be extremely useful to discover security issues, or
    to verify implemented fixes.

    1.  [OWASP ZAP (Zed Attack Proxy)](https://github.com/zaproxy/zaproxy) -
        opensource tool, a good place to start

    or

    2.  [Burp Suite](https://portswigger.net/burp) - commercial tool, extremely
    popular and adequately priced. Has a free edition with limited
    functionality.

### Programming skills:

We think that an application security professional must
have development skills. In the modern world of applications development,
security is not about generic solutions - at least, not anymore. An application
security professional is expected not only to detect security issues, but also
to resolve and/or prevent them. Most of the popular programming
frameworks have security controls built-in; however, they are often not
properly implemented by developers.

**It is no longer the case that developers need to implement security
controls from scratch. Custom security controls implementation and not using
the functionality provided by modern frameworks/well-known libraries will
commonly be the root cause for many security issues you will work with.**

#### Main programming language: **Java**

Widely used by the enterprise, it's not going away anytime soon. Unlike
proprietary technology stacks like Microsoft's (.Net/C#) or Apple's, it's free
to use and learn. Combined with a widespread community of helpful and friendly
developers, Java is a great first language to learn.

If you don't like Java, our other recommendation would be
**[Go](https://golang.org)** - this new language has become very popular in no
time, and it already has a great community. We do see it being used by large
companies, although not as much as Java or .Net

Below is our recommendations on how to start with Java.

##### Theory

Oracle offers great certification paths that provide a very good structure on
how to learn Java. Even if you decide not to take the exam in the end, Oracle's
Java certification resources are a great place to start learning.

1.  Books: Look for study guides to prepare for "Oracle Certified Associate,
    Java SE Programmer" exams. There will be two exams: Associate and
    Professional. This is the required knowledge to be effective with Java.

2.  Mock exams: We recommend Java Mock Exams by
    [Enthuware](http://enthuware.com) to help solidify your Java knowledge. They
    are very cheap, and together with theory in books, spending as little as
    just 10 minutes a day with Mock exams will help learn Java faster.

3.  **[Spring](http://spring.io/)** is probably the best Java framework to begin
    with. It is a popular way to quickly build web applications, has great
    documentation, most companies use it, and it is probably the best
    introduction into the world of modern software development.

    **NOTE**: We consider this to be **the hardest item to learn on this list**,
    so allow some time for reading and practice. The knowledge and skills
    obtained while learning Spring will make you stand out as an application
    security professional.

    Spring quickstart:
    1.  Book:
        "[Spring in action](https://www.manning.com/books/spring-in-action-fourth-edition)"
        is great for getting started with Spring.

    2.  This is a good opportunity for us to stress that **reading reference
        manuals will help make you a better security professional**, so we
        recommend that you read Spring reference documentation in addition to
        the book. It does looks huge, but authors structured it the way that you
        only need to read what's necessary, and you can just index the rest to
        know where to come back to looking for information on specific items.

##### Practice

There is of course nothing better for learning a programming language than to
write programs using it. We just wanted to provide you with a couple of items we
wish we knew when just started to learn programming:

1.  Always use a dependency management (build) tool to write your programs.
    Never download dependencies manually.

    For Java, we strongly recommend learning how to use
    **[Maven](https://maven.apache.org/)**. A great alternative would be
    [Gradle](https://gradle.org/), but it's not yet widely adopted by
    enterprise.

    Start your first Java project by running `mvn archetype:generate` and
    selecting the default template it offers, `maven-archetype-quickstart`.

2.  Always use a version control system.

    We of course recommend **[Git](https://git-scm.com/)**. It is essential to
    know by anyone who is involved in application development.

    Git is very easy to start with:

    1.  There is a free book: <https://git-scm.com/doc>

        Don't be alarmed by the book's size. You only need to read the first
        3 sections: "*Getting started*", "*Git basics*", and "*Git branching*" to
        start. It will take around an hour of your time.

    2.  Git also has very cool tutorials: <https://try.github.io>

3.  We also recommend you to start practicing
    [Test-driven development](https://en.wikipedia.org/wiki/Test-driven_development)
    \- this is one of the most important concepts that you will need to be
    familiar with in your job as an Application Security professional for two
    reasons:

    1.  It helps understand the importance of defining the problem before
        working on a solution, and how to ensure consistency of that solution
        quality over time.
    2.  One of the best ways to inject security requirements into the development process 
        is to add security tests to the software development project and ensure that
        the build does not complete successfully until these tests pass.

    By the way, if you used our advice above and started your project with Maven
    Quickstart archetype, you already have a sample test included in your
    project.

4.  Use [Lint](https://en.wikipedia.org/wiki/Lint_(software)) and code quality
    control.

    These tools are fast, stable, easy-to-use, and they assist in writing
    quality, bug-free code. And if you happen to review someone else's code,
    these tools do help a lot as well.

    Authors of this document use the following linting tools:

    1.  [SonarLint](https://www.sonarlint.org/) - a free IDE plugin that checks
        code quality and highlights potential bugs
    2.  We use [Intellij IDEA](https://www.jetbrains.com/idea/) as our IDE - it
        has embedded code inspections and features which are extremely helpful
    3.  And we probably should mention
        [remark](https://github.com/remarkjs/remark) which we use to collaborate
        on this project

#### Secondary programming language (scripting): **JavaScript**

In addition to their main programming language, a security professional will
always need to write scripts: this can be a quick test, some automation, or even
a solution that injects security into a build pipeline. Scripting commonly
involves items at the operating system level (working with files, directories,
running binaries etc) which are not best addressed by Java or, say, C#.

We recommend JavaScript (aka ECMAScript) and it's interpreter,
[**NodeJS**](https://nodejs.org) for many reasons - it has become extremely popular
in the recent years, and it's much more convenient than
[**Python**](https://www.python.org/), the former champion in this space.
JavaScript is also a major component of any web and mobile application.

#### IT infrastructure skills:

Let us throw a word '
[DevOps](https://aws.amazon.com/devops/what-is-devops/)' in this text - it
is becoming widely adopted by many companies, and the authors of this document are
big fans of this approach.

Application security professionals will need to be familiar with DevOps, which
includes some knowledge of infrastructure - specifically, operation systems
and various cloud providers.

Here's the list of what we recommend to learn:

1.  **GNU/Linux** - a family of free operating systems used (almost)
    everywhere, from software development to running production
    applications. Our recommendation is to start with
    [Debian](https://www.debian.org).

    We should also mention [CygWin](https://cygwin.com) - it makes many of
    GNU/Linux tools available for Windows users. Note that cygwin
    installation does not require admin rights if run with `-B` command line
    parameter: `setup-x86_64.exe -B`

2.  **[Docker](https://www.docker.com)** - Docker is a solution which allows
    applications to be packaged into containers so that all dependencies are
    taken care of, and allows the user to run the container
    instead of spending hours or maybe days in
    [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell).

3.  **[Amazon Web Services](https://aws.amazon.com)** - very popular
    provider for cloud services
