# The best path into Application Security we know

We created this page together with [Will Asciutto](https://github.com/wasciutto)
to share notes from our discussions about what would be the optimal path for
someone new to become an application security engineer.

The goal is not to repeat those excellent guides already made available on the
Internet by both the development and security communities, but to point you to
where and, sometimes, how to start.

## Security - the easiest part

We have a so-called "5+5" formula - one only needs to read around 5 security
books and get familiar with around 5 security-related resources to obtain the
initial knowledge in the security space.

Below are our recommendations on where to start learning.

### Theory

#### Books

1.  [CISSP CBK (Common Body of Knowledge)](https://www.isc2.org/Certifications/CISSP)

    A great material by [(ISC)<sup>2</sup>](https://www.isc2.org) with a wide
    coverage of topics every security professional should be familiar with. It
    also provides a good direction on applying your skills and bringing value to
    the people and organizations you work with.

2.  [CSSLP CBK](https://www.isc2.org/Certifications/CSSLP)

    Another material by (ISC)<sup>2</sup> focused on secure software lifecycle.

    Of course, we recommend reading both the CISSP and CSSLP CBKs (or, even
    better, become a member and get certified). Still, if you really have to
    choose between the two, we recommend CISSP - it will give you a wider
    perspective on security topics to start with.

3.  [Agile Application Security: Enabling Security in a Continuous Delivery Pipeline](http://shop.oreilly.com/product/0636920045106.do)

    A long-awaited book helps understand how one can apply security to the
    modern world of agile software development.

4.  [The Web Application Hacker's Handbook: Finding and Exploiting Security Flaws](https://www.wiley.com/en-us/The+Web+Application+Hacker%27s+Handbook%3A+Finding+and+Exploiting+Security+Flaws%2C+2nd+Edition-p-9781118026472)

    A great source of knowledge about how web applications work and what are
    their security weaknesses.

5.  [The Tangled Web: A Guide to Securing Modern Web Applications](https://nostarch.com/tangledweb)

    Many security professionals recommend this great book about web application
    security.

#### Resources

1.  [OWASP TOP-10](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project)

    The top common application security vulnerabilities list. Note that it's not
    the complete list, and just the top 10. Used by many professionals as a
    baseline to prioritize their work on application security issues.

2.  [OWASP ASVS (Application Security Verification Standard)](https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project)

    [OWASP](https://owasp.org/)'s comprehensive guide on how to verify
    application security. This is where the top 10 list above comes from.
    Probably the most useful resource on Application Security currently
    available.

3.  [MITRE CWE (Common Weaknesses Enumeration)](https://cwe.mitre.org)

    Database of known security weaknesses. We recommend it not only because it
    helps understand both the problem and help with the solution, but also
    because it helps avoid confusion when discussing potential security finding
    between different parties. That's why many security researchers and tools
    map all their findings to CWE IDs.

4.  [Hypertext Transfer Protocol Version 2 (HTTP/2)](https://tools.ietf.org/html/rfc7540)

    HTTP is the protocol web applications use to communicate. Knowledge of this
    protocol is essential for every application security professional.

#### Continuous learning

##### Podcasts

Listening to podcasts is a great way to stay on top of any updates in the world
of application security. We recommend:

1.  [**Security Weekly**](https://securityweekly.com/shows) shows - really great
    guys who now have grown their original podcast, "Paul's Security Weekly,"
    into several shows covering different topics, and we recommend subscribing
    to them all. Lots of useful info and fun.

2.  [**The Secure Developer**](https://www.heavybit.com/library/podcasts/the-secure-developer)
    \- a podcast by [Guy Podjarny](https://twitter.com/guypod), founder of
    [Snyk](https://snyk.io). Great discussions, awesome guests.

3.  [**Application Security PodCast**](https://securityjourney.com/application-security-podcast/)
    \- another great application security podcast. Amazing stories and
    interviews.

### Practice

1.  Complete these challenges to see common vulnerabilities in action:

    1.  [OWASP WebGoat](https://github.com/WebGoat/WebGoat)

    WebGoat has great tutorials and will guide you through everything. Its
    development version also teaches you how to fix common vulnerabilities in
    Java Web Applications. Additional lessons are available at
    [GitHub](https://github.com/WebGoat/WebGoat-Lessons).

    2.  [OWASP JuiceShop](https://github.com/bkimminich/juice-shop)

    JuiceShop is a good example of a modern 'single-page' application
    ([SPA](https://en.wikipedia.org/wiki/Single-page_application)), and it's
    challenges are fun!

2.  Learn to use attack proxies. These tools will help you see all communication
    aspects of web applications, learn how they interact, and how parameters are
    being passed. This will be extremely useful to discover security issues or
    to verify implemented fixes.

    1.  [OWASP ZAP (Zed Attack Proxy)](https://github.com/zaproxy/zaproxy) - an
        OpenSource tool, a good place to start

    or

    2.  [Burp Suite](https://portswigger.net/burp) - commercial tool, extremely
        popular and adequately priced. Has a free edition with limited
        functionality.

    By the way, most modern web-browsers have a similar toolset available in
    their Developer Tools (F12) - check the 'Network' tab.

## Software development - the life's journey:

We think that an application security professional must have development skills.
In the modern world of application development, security is not only about
detecting potential weaknesses and providing generic recommendations. An
application security professional is expected to lead development teams to a
proper solution in each project's specific conditions.

Most of the popular programming frameworks already have security features
built-in. These features are often just not being used - a successful
application security professional will guide developers on using these features
instead of implementing anything from scratch.

**It is no longer the case that developers need to implement security controls
from scratch. Wasting time on reinventing the wheel implementing security
controls from scratch instead of using built-in functionality provided by modern
platforms and frameworks is the most common root cause for application security
issues.**

We recommend the following learning path for your programming skills.

### Main programming language: [**Java**](https://java.com)

Widely used in large companies, it's not going away anytime soon. It's free to
use and a great programming language to learn. There is a big community and lots
of helpful resources on the Internet.

> **NOTE**: The author of this text uses [**Kotlin**](https://kotlinlang.org/)
> as his primary programming language, but I recommend starting with Java if this
> is your first programming language.

Below are our recommendations on how to start with Java.

#### Java - Theory

Oracle offers great [certification paths](https://education.oracle.com/) that
provide an excellent structure on paths to learn Java. Even if you decide not to
take the exam in the end, Oracle's Java certification resources are a great
place to start learning.

1.  Books: Look for study guides to prepare for the "Oracle Certified Java SE
    Programmer" exams. There will be two exams: Associate and Professional. This
    is the required knowledge to be effective with Java.

2.  Mock exams: We recommend Java Mock Exams by
    [Enthuware](http://enthuware.com) to help solidify your Java knowledge. They
    are very cheap, and together with theory in books, spending as little as
    just 10 minutes a day with Mock exams will help learn Java faster.

3.  **[Spring](http://spring.io/)** is probably the best Java framework, to
    begin with. It is a popular way to build applications quickly, and it has
    great documentation. Most companies use it, and it is probably the best
    introduction to the world of modern software development. .

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
        the book. It looks huge, but its authors structured it the way that you
        only need to read what's necessary, and you can index the rest to know
        where to come back to looking for information on specific items.

4.  After you become familiar with Spring Framework, we recommend an extra step:
    now it is a good time to look into **Java Enterprise Edition**. Even if you
    just read the [Tutorial](https://javaee.github.io/tutorial/), this will
    enable you to start working with software developers and help them find the
    best solutions for any security issues they will have. And it will also help
    you advance to a new level in your own projects.

#### Java - Practice

Of course, there is nothing better for learning a programming language than to
write programs using it. We just wanted to provide you with a couple of items we
wish we knew when we just started to learn to program:

1.  Always use a dependency management (build) tool to write your programs.
    Never download dependencies manually.

    For Java, we strongly recommend learning how to use
    **[Gradle](https://gradle.org/)**, a mighty build, and dependency management
    tool. A great alternative would be [Maven](https://maven.apache.org/), the
    previous leader in Java space, which is still very popular in large
    companies.

    Start your first Java project by running `gradle init` or `mvn
    archetype:generate` and selecting the default templates they offer.

2.  Always use a version control system.

    We of course recommend **[Git](https://git-scm.com/)**. It is essential to
    know for anyone who is involved in application development.

    Git is very easy to start with:

    1.  There is a free book: <https://git-scm.com/doc>

        Don't be alarmed by the book's size. You only need to read the first 3
        sections: "*Getting started*", "*Git basics*", and "*Git branching*" to
        start. It will take no more than around an hour of your time.

    2.  Git also has very cool tutorials: <https://try.github.io>

3.  We also recommend you to start practicing
    [Test-driven development](https://en.wikipedia.org/wiki/Test-driven_development)
    \- this is one of the most important concepts that you will need to be
    familiar with on your job as an Application Security professional for two
    reasons:

    1.  It helps understand the importance of defining the problem before
        working on a solution and ensuring consistency of that solution quality
        over time.

    2.  One of the best ways to inject security requirements into the
        development process is to add security tests to the software development
        project and ensure that the build does not complete successfully until
        these tests pass.

    By the way, if you used our advice above and started your project with
    Gradle or Maven, you already have a sample test included in your project.

4.  Use [Linting](https://en.wikipedia.org/wiki/Lint_(software)) and code
    quality control tools.

    These tools are fast, stable, easy-to-use, and they assist in writing
    quality, bug-free code. And if you happen to review someone else's code,
    these tools do help a lot as well.

    Authors of this document use the following linting tools:

    1.  [SonarLint](https://www.sonarlint.org/) - a free IDE plugin that checks
        code quality and highlights potential bugs

    2.  We use [Intellij IDEA](https://www.jetbrains.com/idea/) as our IDE - it
        has embedded code inspections and features which are extremely helpful

    3.  And we probably should mention
        [remark](https://github.com/remarkjs/remark), which we use to
        collaborate on this project

### Secondary programming language (scripting): **JavaScript**

In addition to their main programming language, a security professional will
always need to write scripts: this can be a quick test, automation, or even a
solution that injects security into a build pipeline. Scripting commonly
involves items at the operating system level (working with files, directories,
running binaries, etc.).

We recommend
[ECMAScript](https://www.ecma-international.org/publications/standards/Ecma-262.htm),
aka JavaScript and it's interpreter, Node, for many reasons - it has become
prevalent in recent years, and it's much more convenient than Python, the former
champion in this space. JavaScript is also a major component of any web and
mobile application.

### IT infrastructure skills:

In the world of modern software development, the practice of
[DevOps](https://en.wikipedia.org/wiki/DevOps) is adopted by more and more
organizations bringing in automatic builds and deployment everywhere.

A successful application security professional will need to be able to inject
their security tools into the automation pipeline, and that will not only
require programming and scripting skills, but also knowledge of the stack that
is used to build and run software.

Here's the list of our recommendations:

1.  **[GNU/Linux](https://www.gnu.org/gnu/linux-and-gnu.html)** - a family of
    free operating systems used (almost) everywhere, from software development
    to running production applications. Most continuous build/deployment
    pipelines predominantly use GNU/Linux because it's free, and it was designed
    for this type of task better than any other operating system. We recommend
    starting with [**Debian**](https://www.debian.org) distribution because it's
    straightforward to learn and use in any environment.

    And if you are looking for a good resource to learn GNU/Linux and modern
    operating systems in general, the following two distributions have great
    documentation. Just create a virtual machine and follow their installation
    guides:

    1.  [Arch Linux](https://archlinux.org)
        ([Installation Guide](https://wiki.archlinux.org/index.php/Installation_guide))

    2.  [Gentoo](https://gentoo.org)
        ([Handbook](https://wiki.gentoo.org/wiki/Handbook:Main_Page))

    We should also mention [Cygwin](https://cygwin.com) - it makes many of the
    GNU tools available for Windows users. Note that Cygwin installation does
    not require admin rights if run with `-B` command line parameter:
    `setup-x86_64.exe -B`

2.  **[Docker](https://www.docker.com)** - Docker is a solution that allows
    applications to be packaged into containers, solving problems with
    dependencies, isolation, and deployments. It allows the user to run the
    container instead of spending hours or maybe days trying to get their tools
    working from scratch. The majority of automatic build pipelines use Docker,
    and it's a great way to make security tools available for developers.

    Learning Docker will allow you to enter the modern world of cloud
    technologies and container orchestration.
