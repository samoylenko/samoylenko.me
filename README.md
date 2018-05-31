[![Build Status](https://travis-ci.org/samoylenko/appseclearning.svg?branch=master)](https://travis-ci.org/samoylenko/appseclearning)

# Learning Application Security

This project was created in collaboration Will Ascuitto - we decided to start
collecting notes from our conversations about sharing our knowledge with
colleagues who are just starting their professional career in application
security.

This document contains a list of items which we think may help build the
required skills and knowledge quickly. We also share our practical,
real-world experience and advice with those who want to make a difference and
become and information security professionals able to productively interact with
development teams - a skill which is currently in a very high demand.

## What to learn (and why)

1.  Application Security skills
    1.  Theory
        1.  [OWASP TOP-10](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project)

        The top common application security vulnerabilities list. As you will
        often see, for many of our colleagues application security starts and
        ends here, however this is just the beginning, and is just a small bit
        of what needs to be watched for.

        1.  [MITRE CWE (Common Weaknesses Enumeration)](https://cwe.mitre.org)

        Knowledge base on security weaknesses. Vulnerabilities that are found
        by security researchers are commonly mapped against CWE IDs - this is
        a practice that we recommend to ensure having a common ground with all
        parties involved into vulnerability resolution process.

        3.  [OWASP ASVS (Application Security Verification Standard)](https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project)

        Great guide on what and how to look for in applications.

        4.  [Hypertext Transfer Protocol Version 2 (HTTP/2)](https://tools.ietf.org/html/rfc7540)

        HTTP is the protocol web applications use to communicate. Knowledge of
        this protocol is essential for every application security professional.

    2.  Practice
        1.  Complete these challenges to see common vulnerabilities in action:
            1.  [OWASP WebGoat](https://github.com/WebGoat/WebGoat)

            WebGoat has great tutorials, and will guide you through everything.
             Its development version also enables you to learn how to fix common
             vulnerabilities in Java Web Applications. Additional lessons are
             available at [GitHub](https://github.com/WebGoat/WebGoat-Lessons).

            2.  [OWASP JuiceShop](https://github.com/bkimminich/juice-shop)

            JuiceShop is a very good example of modern 'single-page'
            application, and it's challenges are fun!

        2.  Learn to use this tool, it's very useful:
            1.  [OWASP ZAP (Zed Attack Proxy)](https://github.com/zaproxy/zaproxy)
                (or [Burp Suite](https://portswigger.net/burp) - commercial
                analogue, extremely popular, and adequately priced)

            These tools are very useful for looking into how web applications
            work and for finding and reproducing potential vulnerabilities.
            Use these tools while playing with WebGoat or JuiceShop - it's
            highly recommended!

2.  Programming skills:

    We think that an application security professional must
    have development skills. In the modern world of applications development,
    security is not about generic solutions - at least, not anymore. Application
    security professional is expected to know how to resolve and/or prevent
    security issues - not only detect those. And there will be popular
    frameworks in each programming language, and most probably all required
    security controls will present in these frameworks already, just not
    properly applied by developers.

    **It is not normal anymore if a developer has to implement security
    controls from scratch. In most cases, this (implementing security controls
    from scratch and not using functionality provided by modern frameworks or
    well-known libraries) will be the root cause for many security issues
    you will work with.**

    1.  Main programming language: **Java**

        Widely used by the enterprise, it's not going away anytime soon. And
        unlike **.Net / C#**, it's free to use and learn. Also, it's not
        restricted to just Microsoft stack. Java is a great first language to
        learn, and it also has a friendly and very helpful, huge community.

        If you don't like Java, our other recommendation would be **Go**, but
        it's not currently very popular in the world of enterprise.

        1.  Use a dependency management (build) tool everytime when you are
            writing your programs. Never download dependencies manually.

            For Java, we recommend **[Maven](https://maven.apache.org/)**. A great
            alternative would be [Gradle](https://gradle.org/), but it's not yet
            widely adopted by entherprise.

            Start your first java project by running `mvn mvn archetype:generate`
            and selecting the default template it offers
            (`maven-archetype-quickstart`).

        2.  **[Spring](http://spring.io/)** is probably the best Java framework
        to begin with. It is used to quickly build web applications. And it is
        very popular.

        There's a book which helps start with Spring -
        "[Spring in action](https://www.manning.com/books/spring-in-action-fourth-edition)".
        But it's probably also a good opportunity for us to stress that
        another thing that makes you a better security professional is **reading
        reference manuals**, so we do strongly recommend you to read spring
        reference documents in addition to the book.

        This is probably the **hardest item to learn on this list**, so please
        allow some time for reading and practice. But the knowledge and
        practice obtained while learning Spring is exactly what will make you
        stand out as an application security professional.


    2. Scripting language (secondary programming language): **ECMAScript aka
       JavaScript** (specifically, **[NodeJS](https://nodejs.org/)**)

       In addition to the main programming langunage, a security professional
       will always need to write scripts: It can be a quick test, or some
       automation, or maybe even a solution that injects security into a build
       pipeline. It will involve items commonly at a level of operating system
       (working with files, directories, running binaries etc) which are not
       best addressed by Java or, say, C#.

       We recommend JavaScript for many reasons - it has become extremely
       popular in the recent years, and it's much more convenient than Python,
       which was a champion for us in this space for quite a long time.

       Knowing JavaScript is also a huge bonus because it's now a major
       component of any web and mobile application.


    3. Version Control System (**[Git](https://git-scm.com/)**)

       Git is essential to know by any person who is involved in application
       development.

       Git is easy to start with:

       1. There is a free book: https://git-scm.com/doc
       2. There is a very cool tutorial: https://try.github.io


    4. Use [Lint](https://en.wikipedia.org/wiki/Lint_(software)) and code
       quality control

       We decided to include this section in the document because these tools
       are extremenely easy to use, they are fast and stable, and they really
       help writing good and *secure* code. You can consider these tools
       'cheating' if you like - if you happen to review someone else's code,
       these tools do help a lot.

       There are authors of document use the following tools:
       1. [SonarLint](https://www.sonarlint.org/) - a free IDE plugin that
          checks code quality and highlights potential bugs
       2. We use [Intellij IDEA](https://www.jetbrains.com/idea/) as our IDE -
          it has embedded code inspections and features which are very helpful
          during code reviews
       3. [ESlint](https://eslint.org/) - for JavaScript, as part of automatic
          builds and collaboration
       4. And we probably should mention
          [remark](https://github.com/remarkjs/remark) which we use to
          collaborate on this project

5.  Infrastructure skills:

    Let us throw a word '
    [DevOps](https://aws.amazon.com/devops/what-is-devops/)' in this text - it
    becomes widely adopted by many companies, and authors of this document are
    also big fans of this approach.

    Application security person will need to be familiar with DevOps, which
    includes some knowledge of infrastructure - specifically, operation systems
    and various cloud providers.

    Here's the list of we recommend to learn:

    1.  **Linux** - free operating system. Our recommendation is to start with
        [Debian](https://www.debian.org/) (easy to use and learn) or
        [CentOS](https://www.centos.org/) (it's very similar to RedHat, widely
        used by enterprise)

        We should also mention that we use Linux a lot, and even at Windows
        environments we have [CygWin](https://cygwin.com) installed - it
        provides access to vital linux binaries (such as
        [curl](https://curl.haxx.se), for example)

        Note that cygwin installation does not require admin rights for
        installation if run with -B command line parameter: `setup-x86_64.exe
        -B`

    2.  **[Docker](https://www.docker.com)** - docker is a solution which allows
        to package applications in containers so that e.g. all dependencies are
        taken care of, and all user needs to do is to just run the container
        instead of spending hours or maybe days in
        [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell).

    3.  **[Amazon Web Services](https://aws.amazon.com)** - very popular
        provider for cloud services
