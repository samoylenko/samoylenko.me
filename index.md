# What is Application Security?

Let's not waste your time: **Application Security
is [Continuous Delivery](https://www.youtube.com/watch?v=ulRCs7xQA74),
[Continuous Delivery](https://www.youtube.com/watch?v=ulRCs7xQA74) is
Application Security**. You get there by shipping code rapidly,
shortening the feedback loop, embracing change, experimenting and
learning.

I can no longer distinguish between security
issues and other software bugs, both in design and code. Just priority and
complexity, maybe - and that's what I base my following statement on:

**Application security engineers are software engineers**. If you are a
pentester, an "offensive security" professional that never shipped code, you are
part of Quality Assurance. The "glorious" days of "hackers telling developers
what to do" are long gone and proven wrong tenfold.

## What is a secure application?

> A secure application is an application that only does what it was designed to
> do and nothing else.
>
> -- Someone at the [Security Weekly](https://securityweekly.com/) podcast

(I apologize for not remembering, who and when said this, but this is the best
definition I could find so far.)

## What is an application security issue (vulnerability)?

Security issues are unplanned, undesired, and unexpected application behavior.

## Where do application security issues come from?

They come from what is entirely normal and natural to all humans - exercising
our right to make mistakes and not always be perfect at everything.

## What causes software engineers to make more mistakes?

> If I'm doing something myself, I'm probably doing it wrong
>
> -- [Kyle Randolph](https://twitter.com/kylerandolph),
> at [The Secure Developer podcast, ep. #1](https://www.heavybit.com/library/podcasts/the-secure-developer/ep-1-prioritizing-secure-development/)

The most common ways to make more mistakes I see:

1.  ["**Reinventing the wheel**"](https://en.wikipedia.org/wiki/Reinventing_the_wheel)
    and the resulting unnecessary additional complexity - such as taking on
    work (and assuming the corresponding responsibility) that is out of the
    original project (or task) scope.

2.  **Making decisions in isolation** - in the world of instant communication and
    the Internet, assuming that you are the first to face this problem and that
    no one else hasn't solved it. And in the rare scenario when there is no
    existing solution, thinking that you already have enough knowledge and
    resources to solve it without the help of others.

(Indeed I am aware that the two items below can actually be merged into one)

### But is there a checklist?

The best one I know is
[**OWASP Application Security Verification Standard**](https://github.com/OWASP/ASVS).
There are over 200 items on that list, but just following the modern software
development practices, avoiding the two abovementioned mistakes, and simply
reading manuals for the tools and libraries or frameworks you are using covers
most of them.

Some people call it "**Secure Coding Practices**." But it looks like there is no
universal document I could refer you to, and each company (or team) defines its
own. Here's [my attempt to define something like that](practices).

## Still reading?

Let's continue our discussion:

*   [Preventing human mistakes in software development](prevent)
*   [Learning Application Security](learn)
*   [Secure Coding Practices](practices)
