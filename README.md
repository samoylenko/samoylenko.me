[![Build Status](https://travis-ci.org/samoylenko/appseclearning.svg?branch=master)](https://travis-ci.org/samoylenko/appseclearning)

# Learning Application Security

This project was created in collaboration with Will Ascuitto - we decided to start
collecting notes from our conversations about sharing our knowledge with
colleagues who are just starting their professional career in application
security.

This document contains a list of items which we think may help build the
required skills and knowledge quickly. We also share our practical,
real-world experience and advice with those who want to make a difference and
become and information security professionals able to productively interact with
development teams - a skill which is currently in a very high demand.

## What to learn (and why)

Becoming an application security professional requires working knowledge in at
least two areas: computer security and software development.

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
understanding of what to look for when you will be exploring software
development domain.

Below are our recommendation on where to start learning.

#### Theory

##### Books

1.  [CISSP CBK (Common Body of Knowledge)](https://www.isc2.org/Certifications/CISSP)

A great book by [(ISC)<sup>2</sup>](https://www.isc2.org) which not only
contains everything that security professional should know, but also provides a
good direction on how to apply your skills and bring value to people or
organizaitons you will work with.

2.  [CSSLP CBK](https://www.isc2.org/Certifications/CSSLP)

Another CBK by (ISC)<sup>2</sup> focused on software lifecycle.

We of course recommend reading both the CISSP and CSSLP CBKs (or, even better,
become (ISC)<sup>2</sup> member and get certified), but if you really have to
chose between the two, we recommend CISSP - it will give you a wider perspective
on security topics to start with.

3.  [The Web Application Hacker's Handbook: Finding and Exploiting Security Flaws](https://www.wiley.com/en-us/The+Web+Application+Hacker%27s+Handbook%3A+Finding+and+Exploiting+Security+Flaws%2C+2nd+Edition-p-9781118026472)

Some great penetration testers we met call this book their Bible of hacking and
keep it at their desk at all times.

4.  [The Tangled Web: A Guide to Securing Modern Web Applications](https://nostarch.com/tangledweb)

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

There are fun ways to stay on top of security news. We recommend the following
podcasts, because they are not boring and are quite motivational:

1.  [Security Weekly](https://securityweekly.com/shows) - really great guys who
    now have grown into a number of separate shows that we recommend subscribing
    to all of them. Lots of extremely useful info and fun.

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

1.  Main programming language: **Java**

Widely used by the enterprise, it's not going away anytime soon. Unlike **.Net /
C#**, it's free to use and learn. Also, it's not restricted to the Microsoft
stack. Combined with a widespread community of helpful and friendly developers,
Java is a great first language to learn.

If you don't like Java, our other recommendation would be **Go**, but
it's not currently very popular in the world of enterprise.

1.  Use a dependency management (build) tool to write your programs.
    Never download dependencies manually.

    For Java, we recommend **[Maven](https://maven.apache.org/)**. A great
    alternative would be [Gradle](https://gradle.org/), but it's not yet
    widely adopted by entherprise.

    Start your first java project by running `mvn mvn archetype:generate`
    and selecting the default template it offers
    (`maven-archetype-quickstart`).

2.  **[Spring](http://spring.io/)** is probably the best Java framework to begin
    with. It is a popular way to quickly build web applications, has great
    documentation, and it will introduce you into the world of modern software
    development.

We consider this to be the **hardest item to learn on this list**, so allow some
time for reading and practice. The knowledge and skills obtained while learning
Spring will make you stand out as an application security professional.

"[Spring in action](https://www.manning.com/books/spring-in-action-fourth-edition)"
book is great for getting started with Spring.

This is a good opportunity for us to stress that **reading reference manuals**
will help make you a better security professional, so we recommend that you read
Spring reference documentation in addition to the book.

2.  Scripting language (secondary programming language): **ECMAScript aka
    JavaScript** (specifically, **[NodeJS](https://nodejs.org/)**)

    In addition to their main programming language, a security professional will
    need to write scripts: this can be a quick test, some automation, or even a
    solution that injects security into a build pipeline. Scripting commonly
    involves items at the operating system level (working with files,
    directories, running binaries etc) which are not best addressed by Java or,
    say, C#.

    We recommend JavaScript for many reasons - it has become extremely
    popular in the recent years, and it's much more convenient than Python,
    the former champion in this space. JavaScript is also a major
    component of any web and mobile application.

3.  Version Control System (**[Git](https://git-scm.com/)**)

    Git is essential to know by anyone who is involved in application
    development.

    Git is easy to start with:

    1.  There is a free book: <https://git-scm.com/doc>
    2.  Git has very cool tutorials: <https://try.github.io>

4.  Use [Lint](https://en.wikipedia.org/wiki/Lint_(software)) and code
    quality control

    We decided to include this section because these tools
    are fast, stable, easy-to-use, and help writing quality, _secure_ code.
    You can consider these tools 'cheating' if you like -
    if you happen to review someone else's code, these tools do help a lot.

    Authors of this document use the following tools:

    1.  [SonarLint](https://www.sonarlint.org/) - a free IDE plugin that
        checks code quality and highlights potential bugs
    2.  We use [Intellij IDEA](https://www.jetbrains.com/idea/) as our IDE -
        it has embedded code inspections and features which are helpful
        during code reviews
    3.  [ESlint](https://eslint.org/) - for JavaScript, as part of automatic
        builds and collaboration
    4.  And we probably should mention
        [remark](https://github.com/remarkjs/remark) which we use to
        collaborate on this project

5.  IT infrastructure skills:

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
