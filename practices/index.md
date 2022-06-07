# Secure Coding Practices

As far in the past as I can remember, vulnerability remediation was always a
significant part of my job, regardless of the role I had. Assisting development
teams in remediating already known vulnerabilities could easily take up to 30-40
percent of all my time in any capacity. And what I still cannot comprehend is
when I open another software project that requested assistance with remediation,
in my IDE, the code all lights up with warnings, suggestions, quality issues,
and sometimes even errors.

My first instinct was to think, "how can we start talking about the security of
the project when it has no basic code quality control?" In time, I attempted to
define what "basic code quality control" actually means, and I tried to create
something like the old-school "You must be this tall to ride" initiative. With
predictable results - that was still the "always no" classic security approach.
And there are already existing great resources such
as [OWASP OpenSAMM](https://owaspsamm.org/model)
or [BSIMM](https://www.bsimm.com/). But since then, I have been trying to create
a basic list of the specific controls and tools that meet these requirements.

Everything I could find on the Internet so far requires software engineers to
spend an enormous amount of extra time learning all those items and implies
creating controls from scratch - which I think should not be the case anymore. I
am convinced that in the past 10-15 years, the world of modern software
development has learned a lot about security and has embedded time-tested robust
security solutions in the popular modern platforms and frameworks.

That is proven by a fascinating fact - in the recent five years, whenever I was
working with development teams to remediate vulnerabilities, it usually resulted
in reducing code and complexity and not adding the security controls written
from scratch but merely enabling what was already available as part of the
platform or framework they used.

And now, there is only one bridge left to build before getting into the essence
of what I believe to be modern secure coding practices. Here it is.

## Modern secure coding practices facts

My vision of Secure Coding Practices is all about:

### Focusing on the value to the business

Most application security controls don't need to be implemented from scratch,
most modern frameworks and platforms already have security controls implemented
by teams of brilliant engineers who have spent years improving and field-testing
those controls. As a result:

-   **Most projects' goal is to enable the business, help the client, and not
    develop security controls from scratch**. So unless we are developing a new
    platform or framework, we shouldn't be wasting time and resources trying to
    reinvent the wheel.

-   It's crucial, however, to follow **rigorous hygiene on the project
    dependencies** - everything from libraries to build tools (see the
    software supply chain issue). At a minimum, restricted to using **only
    well-known and time-tested tools and libraries**, followed by **keeping
    dependencies up to date** and **automated testing** to ensure updates don't
    break the application.

### Employing as much help as possible via automation and collaboration

The project should employ as much as possible help from both automation tools
and human participants in everything from enforcing code style and testing
coverage, all the way to pair programming and any other forms of code and design
reviews. [**This philosophy is discussed in detail here**](../prevent). I
believe that
the best path there is by **embracing the DevOps methodology**, which is based
on
the experience of the modern software development community (and is the best way
to reduce security issues I that know).

### Following modern security and development practices

As of today, the best checklist on security controls that must be present in
software I could find is [**OWASP ASVS**](https://github.com/OWASP/ASVS). The
trick
is - it's over 200 items that require an earnest effort to know and follow it.
But the good news is - simply following the modern development methodologies and
using well-known solutions takes care of the most of security controls in most
software projects.

I, of course, can't possibly pretend to be the one to teach you modern
development methodologies.
Try [Dave Farley](https://www.youtube.com/c/ContinuousDelivery) or
[The Hacker Family](https://www.youtube.com/channel/UCQHbfQOTapMI3EJdN1fQJPg).
But I can share the basics that I learned the hard way by working with dozens of
projects in multiple companies during the last decade or so.

## My approach

This public and personal page is ongoing work, and I still may be missing
something. Secure coding practices that I create for my employers contain more
items, and I adjust them for the specific environment of the individual
company (something like "Always use Artifactory for your dependencies and
artifacts"). But it's no secret what I am using - so you can try, too. Here's
the default logic I am using:

1.  Every security finding contains a [CWE](https://cwe.mitre.org/) reference.
2.  CWE reference is mapped to Secure Coding Practices.
    -   Using CWE in Secure Coding Practices allows embedding Secure Coding Practices in vulnerability reports and dashboards.
3.  Secure Coding Practices are created using (and practices refer to it):
    1.  Company's shared security solutions (and the corresponding architectural
        guidelines)
    2.  [OWASP ASVS](https://github.com/OWASP/ASVS/) (also has CWE mapping)
    3.  [The Twelve-Factor App](https://12factor.net/) (actually, as of recently
        I am mostly using  
        ["Beyond the 12 Factor App" by Kevin Hoffman](http://pivotal.io/beyond-the-twelve-factor-app))
    4.  [OWASP OpenSAMM](https://owaspsamm.org/) and [NIST SSDF](https://csrc.nist.gov/projects/ssdf)
        -   These two are usually already embedded with the company's Information Security Policy (and the derived standards), so the links typically lead directly to the policy portal.

Below goes my personal public draft:

### Secure Coding Practices

1.  **Never put secrets and other sensitive information in your code repository
    or build artifacts. Not even if you encrypt it.**
    -   No sensitive information belongs to your code or artifact. Instead, it
        belongs to the environment configuration, which is dynamic, allowing
        injecting secrets and other configuration parameters during deployments.
        Most modern deployment tools support this approach out of the box. The
        most common patterns are environment variables and file templates.

2.  **Focus on creating value. Don't waste time reinventing the wheel. Use
    managed services as much as possible**
    -   Use cloud and SaaS, and there are so many open source products that
        provide the most needed tools and services for software projects. If your
        project is internal to the company, it (company) has probably already
        invested in the best products and teams of professionals to provide you
        with compliant, secure, and reliable managed services for everything you
        need.

3.  **Employ automation whenever possible, to eliminate the potential human
    error**
    -   The software industry has proven that automation and tests are worthy
        investments that pay ten times over.
    -   Quick checklist:
        -   Dependency management automation
        -   Build automation
        -   Code style, linters and quality checks.
        -   Test automation and coverage
        -   Deployment automation
        -   Security scans
        -   Automatic dependency upgrades

4.  **Verify all new dependencies before adding them to the project**
    -   This includes everything - from libraries and tools to services.
    -   Red flags:
        -   Dependencies that are not well-known or popular and have few or no
            users.
        -   Dependencies with a small number of maintainers (and not backed by
            companies).
        -   Dependencies that are not updated by their maintainers and have
            abandoned open issues and pull requests
        -   Dependencies that are new and didn't have at least 1-2 stable
            releases.
      
5.  **RTFM!**
    -   Once you did a good job ensuring that you only got the best, most
        well-known, and time-tested dependencies for your project, they probably
        already have all the necessary security controls embedded and even enabled
        by default. Hence, all left is not to screw that up. Take time to read the
        tool's manual.
    -   The vast majority of the vulnerabilities I helped fix in
        the last ten years were precisely that - the team was simply unaware of
        their framework's security features.

6.  **Update and patch all project dependencies often**
    -   Most dependencies and dependency managers follow and support
        the [Semantic Versioning](https://semver.org/) model, and if you are
        concerned about breaking changes, you can restrict to the latest patches
        and minor updates.

7.  **Keep development dependencies separate from production ones, and ensure
    that the development functionality does not get in production artifacts**
    -   Most dependency management and build tools allow for separate lists for
        development and test dependencies.

8.  **Use an issue tracker**
    -   Projects of any size need a way to plan, track and prioritize all the
        things that need to be done.
    -   Modern issue trackers are easy to embed in the software development
        process, including tracking commits, pull requests, and releases
        corresponding to specific issues.

9.  **Ensure that your automatic builds don't leak secrets and any other
    sensitive information**
    -   This is one of the most common places to leak sensitive information. Per
        most standards, leaked passwords are considered compromised and are
        required to be changed. The "Internal Threat" scenario includes an
        accidental use of those passwords as well.

10. **Open access to your code repository**
    -   The more people can look at your code, the more chances they spot an issue
        or contribute.
    -   There is practically no excuse not to open the code repository to at least
        all other dev teams in the company.

11. **Ensure the project has documentation. At least a quickstart**
    -   Provide at least enough information for a new person to join the project
        to get the build to work locally. This is a necessary first step for
        anyone to contribute to the project in any capacity.

12. **Use [Trunk Based Development](https://trunkbaseddevelopment.com/) and
    establish a code review process**
    -   A prevalent way is to use pull requests.
    -   But check
        out [great alternatives](https://www.youtube.com/watch?v=ASOSEiJCyEM),
        like [pair programming](https://en.wikipedia.org/wiki/Pair_programming).
        Modern IDEs [already have](https://www.jetbrains.com/code-with-me/)
        support for that embedded.

## Next steps from here

*   [Preventing human mistakes in software development](../prevent)
*   [Learning Application Security](../learn)
