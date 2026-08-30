# How to use vulnerability brocards

Vulnerability brocards are meant to help you make
a _quick, initial_ evaluation of a vulnerability report.

They can help you save your time, energy, and sanity
by not having to re-litigate each report from first
principles.

They can help you decide whether or not to continue
triaging the report, or whether you can safely close
it. For example, _inter alia_, a vulnerability brocard
might help you triage a report as:

- Out of scope ("that's something another tool should do")
- Intended behavior ("we document it as working that way")
- A non-security bug ("that's broken, but it doesn't need a CVE")

The correct way to use vulnerability brocards is to
_evaluate the submitted evidence_ against them: you should take
the claims provided by the reporter, and see if they run afoul
of one or more brocards.

If they do, you can _probably_ close the report without further triage,
saving yourself from needing to analyze the report from first
principles.

## Practical use

The above is very abstract. Here's a practical example of applying
a vulnerability brocard, using Alice (a vulnerability triager)
and Bob (a vulnerability reporter):

> **Bob**: I found a vulnerability in LibreWidgets v1.2.3. I can make
> a user who has LibreWidgets installed run arbitrary code controlled
> by an attacker.
>
> **Alice**: What is the mechanism that results in arbitrary code execution?
>
> **Bob**: LibreWidgets loads configuration from the user's home directory
> via a file named `config.py`. If the attacker can write Python
> into that file, they can run arbitrary code.
>
> **Alice**: Yes, our configuration is currently defined as a Python
> script, which means that it runs arbitrary code by design.
> Please see our docs for an explanation of how that works and
> [VB005]() for why that means we don't consider that a report-worthy
> security concern. Did your report have something in mind besides that?
>
> **Bob**: No, that's what I had in mind.
>
> **Alice**: Okay, we're going to close this report as out-of-scope then.

## How _not_ to use vulnerability brocards

It's important to only use vulnerability brocards for _triage_,
not as categorical or universal truths.

Vulnerability reporting and triage involves human (and/or LLM)
communication, which can be imprecise. Good-faith reporters
should be allowed to explain why a brocard might not apply to their
report, rather than having the report summarily dismissed after
an initial evaluation.

## A note on audience

The primary intended audience of this website is people doing
_open source_ vulnerability triage.

With that, let's take a look at the [brocards](./brocards).
