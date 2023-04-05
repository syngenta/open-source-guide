# Open Source Software (OSS) Guide

**NOTE:** This document is neither legal nor comprehensive advice. It should not be taken as such.

- [Introduction](#introduction)
- [OSPO (Open Source Program Office) team](#ospo-open-source-program-office-team)
- [Why should we pay attention to properly using open-source software?](#why-should-we-pay-attention-to-properly-using-open-source-software)
- [Why should we contribute to open-source?](#why-should-we-contribute-to-open-source)
- [How to use open-source code in closed-source projects](how-to-use-open-source-code-in-closed-source-projects.md)
- [How to contribute to open source](how-to-contribute-to-open-source.md)
- [How to open source our code](how-to-open-source-our-code.md)
- [Notes](#notes)

## Introduction

> Open-source software (OSS) is computer software that is released under a license in which the copyright holder grants users the rights to use, study, change, and distribute the software and its source code to anyone and for any purpose.
>
> [https://en.wikipedia.org/wiki/Open-source_software](https://en.wikipedia.org/wiki/Open-source_software)

It's impossible to find or create any modern software that does not rely on open-source code in its foundation.

We heavily use open-source code to develop software for both internal users and external clients and depend on it in our operations.

This guide will try to cover three main questions:

1. [How to properly use open-source code in closed-source projects?](how-to-use-open-source-code-in-closed-source-projects.md)
2. [How to properly contribute to open-source?](how-to-contribute-to-open-source.md)
3. [How to open source our code?](how-to-open-source-our-code.md)

## OSPO (Open Source Program Office) team

The OSPO team is an informal team of open-source enthusiasts and advocates in Syngenta.

We are working with R&D and digital teams to educate and assist them with:

- open-sourcing their code;
- contributing to open-source projects;
- applying the best community and industry standards and practices for their open-source projects;
- guiding on Open Source Software (OSS) licensing.

We are glad to help you with any questions you may have about open-source, licensing, best practices, etc. Talk to us via [ospo@syngenta.com](mailto:ospo@syngenta.com) email or MS Teams chat.

## Why should we pay attention to properly using open-source software?

**TL;DR — violation of OSS licenses may lead to lawsuits, fines, and reputation losses for the company.**

Open-source software doesn't always mean we can freely use it in our projects — **open-source ≠ free**.

There are tens of different [OSS licenses](https://en.wikipedia.org/wiki/Comparison_of_free_and_open-source_software_licenses#General_comparison). Different licenses have [different permissions, conditions and limitations](https://choosealicense.com/licenses/) for use.

Some of them, such as [MIT License](https://choosealicense.com/licenses/mit/), are **permissive** — you are allowed to do almost anything. But you must keep the License text and copyright notice.

Others, such as [GNU AGPLv3](https://choosealicense.com/licenses/agpl-3.0/) are **strictly copyleft**. Using GNU AGPLv3 licensed library in your project — automatically requires you to open-source your project's code under the same GNU AGPLv3 license. Missing this requirement will result in a license violation — possible lawsuits, fines, and reputations losses for the company.

Some OSS software may have **commercial-only** licenses. This means that even if the code of such a library is open-sourced, we can't use it in our projects without buying a commercial license.

Using some Open Source License Scanning Tool (OSS License Scanner) is highly recommended to check if your project uses open-source code properly. It could be a 3-rd party service or a self-hosted tool — choose based on your project's needs and technology stack.

## Why should we contribute to open-source?

There are many ways we could contribute to open-source:

- Upstream our changes/features/fixes to open-source libraries.
- Publishing some of our code as open-source:
  - our infrastructure and helper libraries (frameworks, etc.);
  - client libraries for Syngenta's products;
  - client libraries for third-party products (ORMs, wrappers, etc.);
  - scientific code in the R&D environment.

### Benefits of open-sourcing our projects and code

- Contributions are valuable to the open-source community. It's a meaningful way to support open-source projects and the community.
- Collaborating with scientific research communities and other industrial organizations via open-source projects would benefit all parties and our industry.
- Upstreaming our changes/features/fixes reduces maintenance costs as we don't need to update our forks constantly.
- Some of our open-sourced code may receive valuable support and improvements from the open-source community.
- We may not always be able to justify the continued internal support and development of our internal code and tools. Open-sourcing such code and tools helps to preserve and continuously improve our work. This is particularly valid for scientific code.

### Considerations for open-sourcing our projects and code

- We should ensure that open-sourcing code will not disclose information, know-how or code that gives us a significant competitive advantage.
- We must be sure that we do not release code that does not belong to us.
- In general, we do not open source highly-specific code that we expect not to be helpful for the community.

## How to use open-source code in closed-source projects

[How to use open-source code in closed-source projects](how-to-use-open-source-code-in-closed-source-projects.md)

## How to open source our code

[How to open source our code](how-to-open-source-our-code.md)

## How to contribute to open source

[How to contribute to open source](how-to-contribute-to-open-source.md)

## Notes

1. Inspired by [GitLab's Handbook OSS Guide](https://about.gitlab.com/handbook/engineering/open-source/).
2. Parts of this document are taken from Syngenta's "Open Source Release Checklist (R+D) 2013".
