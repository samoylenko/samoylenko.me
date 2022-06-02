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
creating controls from scratch - which I think is entirely wrong. I am convinced
that in the past 10-15 years, the world of modern software development has
learned a lot about security and has embedded time-tested robust security
solutions in the popular modern platforms and frameworks.

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

-   It's crucial, however, to follow **rigorous hygiene on what is being added
    to the project** - everything from libraries to build tools (see the
    software supply chain issue). At a minimum, restrict to using only
    well-known and time-tested tools and libraries.

### Employing as much help as possible via automation and collaboration

The project should employ as much as possible help from both automation tools
and human participants in everything from enforcing code style and testing
coverage, all the way to pair programming and any other forms of code and design
reviews. [**This philosophy is discussed in detail here**](prevent). I believe that
the best path there is by **embracing the DevOps methodology**, which is based on
the experience of the modern software development community (and is the best way
to reduce security issues I that know).

### Following modern security and development practices

As of today, the best checklist on security controls that must be present in
software I could find is [**OWASP ASVS**](https://github.com/OWASP/ASVS). The trick
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

## Secure Coding Practices List

(Work in progress)

## Next steps from here

*   [Preventing human mistakes in software development](prevent)
*   [Learning Application Security](learn)

