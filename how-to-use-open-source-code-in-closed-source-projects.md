# How to use open-source code in closed-source projects

- [Introduction](#introduction)
  - [Shipped software](#shipped-software)
    - [Allowed to use in shipped software](#allowed-to-use-in-shipped-software)
    - [Not allowed to use in shipped software](#not-allowed-to-use-in-shipped-software)
    - [Allowed with caution to use in shipped software](#allowed-with-caution-to-use-in-shipped-software)
  - [SaaS backend](#saas-backend)
    - [Allowed to use in SaaS backend](#allowed-to-use-in-saas-backend)
    - [Not allowed to use in SaaS backend](#not-allowed-to-use-in-saas-backend)
  - [Non-production software](#non-production-software)
    - [Allowed to use in non-production software](#allowed-to-use-in-non-production-software)
    - [Not allowed to use in non-production software](#not-allowed-to-use-in-non-production-software)
- [Appendix](#appendix)
  - [Approved list of permissive licenses](#approved-list-of-permissive-licenses)
  - [Acceptable only for SaaS backend and non-production use](#acceptable-only-for-saas-backend-and-non-production-use)

## Introduction

**TL;DR: We must always consider the open-source code licenses used in our closed-source projects. Open-source ≠ free. Violation of OSS licenses may lead to lawsuits, fines, and reputation losses for the company.**

Open-source software is a foundation — we use a vast number of open-source libraries in our closed-source projects. We use them in our infrastructure, in our helper libraries, in our client libraries, and in our scientific code.

It's crucial to use open-source code properly and respect the license of the open-source code used.

We could split our closed-source projects into three categories:

- [Shipped software](#shipped-software)
- [SaaS backend](#saas-backend)
- [Non-production software](#non-production-software)

### Shipped software

Any code shipped to the user (in binary or source) is considered shipped software.

Typically, shipped software is:

- mobile apps;
- desktop apps;
- frontend code (JS).

#### Allowed to use in shipped software

Only libraries with **permissive** licenses (for example [MIT License](https://choosealicense.com/licenses/mit/), [Apache 2.0 License](https://choosealicense.com/licenses/apache-2.0/)) could be used safely in our closed-source projects that are considered to be shipped software.

It's highly recommended to use only libraries with licenses from a [approved list of permissive licenses](#approved-list-of-permissive-licenses). Libraries or code with other permissive licenses may be used, but you must check their license first and contact the OSPO team if any doubts arise.

Also, you must adequately put information about all the OSS libraries used in your project. **Users should be able to find the list of all OSS libraries and code used in the project.**

#### Not allowed to use in shipped software

Some OSS libraries have non-permissive **copy-left** licenses, such as [GNU GPLv3](https://choosealicense.com/licenses/gpl-3.0/). You are legally required to distribute the complete source code of your project if any library with such a non-permissive license is used in your project.

Using libraries with copy-left licenses in closed-source projects shipping software is prohibited.

> **Note:** Any code (from blogs, books, etc.) must be treated as copyrighted and not allowed to use in closed-source projects unless an appropriate OSS license is explicitly specified or you have explicit permission from the author.

#### Allowed with caution to use in shipped software

Some copy-left licenses could be used in closed-source projects. For example, GNU LGPLv3.
But you should be very precise in the way you use those libraries to use them strictly accordingly to the license requirements (and it may be hard or impossible in some cases).

- try to avoid using any libraries with copy-left licenses in shipped software;
- if it's crucial to use a particular GPL LGPLv3 library, it's important to talk to the OSPO team to ensure that you are using them correctly.

### SaaS backend

In the case of a SaaS (software-as-a-service) backend, code is only running on our servers. We are not shipping our code or binaries to the user. End-users communicate with the SaaS backend via the network.

#### Allowed to use in SaaS backend

It's allowed to use OSS libraries with permissive licenses such as [MIT License](https://choosealicense.com/licenses/mit/) or [Apache 2.0 License](https://choosealicense.com/licenses/apache-2.0/) ([approved list of permissive licenses](#approved-list-of-permissive-licenses)), **plus** some OSS libraries with copy-left licenses such as [GNU GPLv3](https://choosealicense.com/licenses/gpl-3.0/).

#### Not allowed to use in SaaS backend

Some libraries have **strictly copy-left** licenses, that treat "Network use" as distribution. For example, [GNU AGPLv3](https://choosealicense.com/licenses/agpl-3.0/). You are legally required to distribute the complete source code of your SaaS project backend under the GNU AGPLv3 license if any library with the GNU AGPLv3 license is used in your project.

We must be sure that we **don't use GNU AGPLv3** or a similar license in our closed-source SaaS backend.

> **Note:** Any code (from blogs, books, etc.) must be treated as copyrighted and not allowed to use in closed-source projects unless an appropriate OSS license is explicitly specified or you have explicit permission from the author.

### Non-production software

Code used only for R&D, development or test purposes and does not shipped or communicate via the network with end-users is considered non-production software.

For example:

- bundlers/packers;
- testing and debugging libraries included only in the test/development environment;
- code analyzing tools;
- R&D code that is used only for internal purposes.

#### Allowed to use in non-production software

Both **permissive** and **copy-left** licensed libraries are allowed to use.

> Non-production software may become production software in the future (shipped to the users or became a part of SaaS backend). Some libraries that were allowed in non-production software may be not allowed in production software. Always consider this possibility and check the license of the library before using it in non-production software.

#### Not allowed to use in non-production software

You should be always aware of all your dependencies and their licenses:

- Some OSS-licensed libraries have dual licensing and must be licensed for use in commercial projects. We could use them, but a license must be acquired, the same as for any commercial software.
- Any code (from blogs, books, etc.) must be treated as copyrighted and not allowed to use in closed-source projects unless an appropriate OSS license is explicitly specified or you have explicit permission from the author.

## Appendix

### Approved list of permissive licenses

Libraries with the following permissive licenses are allowed for use in closed-source projects:

- [MIT License](https://choosealicense.com/licenses/mit/): A permissive (non-copyleft) license as defined by the Open Source Initiative.
- [Apache 2.0 License](https://choosealicense.com/licenses/apache-2.0/): A permissive license that also provides an express grant of patent rights from contributors to users.
- [BSD 2-Clause License](https://opensource.org/licenses/BSD-2-Clause): A permissive (non-copyleft) license as defined by the Open Source Initiative.
- [BSD 3-Clause License](https://opensource.org/licenses/BSD-3-Clause) (also known as New BSD or Modified BSD): A permissive (non-copyleft) license as defined by the Open Source Initiative
- [ISC License](https://opensource.org/licenses/ISC) (also known as the OpenBSD License): A permissive (non-copyleft) license as defined by the Open Source Initiative.
- [Ruby 1.8 License](https://github.com/ruby/ruby/blob/ruby_1_8_6/COPYING): Dual-licensed under either itself or the GPLv2, defer to the Ruby License itself. Acceptable because of point 3b: "You may distribute the software in object code or binary form, provided that you do at least ONE of the following: b) accompany the distribution with the machine-readable source of the software."
- [Ruby 1.9 License](https://www.ruby-lang.org/en/about/license.txt): Dual-licensed under either itself or the BSD 2-Clause License, defer to BSD 2-Clause.
- [Creative Commons Zero (CC0)](https://creativecommons.org/publicdomain/zero/1.0/): A public domain dedication.
- [Unlicense](https://unlicense.org): A public domain dedication.
- [OWFa 1.0](http://www.openwebfoundation.org/legal/the-owf-1-0-agreements/owfa-1-0): An open-source license and patent grant designed for specifications.

You are welcome to talk to the OSPO team to add more licenses to this list.

#### Acceptable only for SaaS backend and non-production use

**Some** non-permissive licenses are allowed for use in SaaS (software-as-a-service) backend code that runs only on our servers and in non-production code.

For example:

- [GNU GPLv2](http://www.gnu.org/licenses/gpl-2.0.txt), [GNU GPLv3](http://www.gnu.org/licenses/gpl-3.0.txt), [GNU LGPLv3](https://choosealicense.com/licenses/lgpl-3.0/) are acceptable.
- But not [GNU AGPLv3](https://choosealicense.com/licenses/agpl-3.0/) for SaaS backend (and with big caution for non-production code).

Consider consultation with the OSPO team in such cases.
