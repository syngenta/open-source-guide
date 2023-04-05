# How to open source our code

- [Introduction](#introduction)
- [Principles](#principles)
- [Choose an OSS license](#choose-an-oss-license)
  - [MIT License](#mit-license)
  - [GNU GPLv3 License](#gnu-gplv3-license)
- [Checklist](#checklist)
- [Publishing to GitHub](#publishing-to-github)
- [Appendix](#appendix)
  - [Checklist](#checklist)
  - [How to apply MIT License terms to the new software](#how-to-apply-mit-license-terms-to-the-new-software)
  - [How to apply GNU GPLv3 terms to the new software](#how-to-apply-gnu-gplv3-terms-to-the-new-software)

## Introduction

Follow the next steps to open-source your code:

1. Check [principles](#principles).
1. [Choose an OSS license](#choose-an-oss-license).
1. Complete the [checklist](#checklist) and receive approval.
1. [Publishing to GitHub](#publishing-to-github).

## Principles

The main principle is: **Ensure open-sourcing your code will not damage Syngenta**.

The key areas to be assessed are:

- The release of the code will not be to Syngenta’s competitive disadvantage or detriment to Syngenta’s business goals.
- We can release the Source Code as Open Source Software without infringing any other parties' license or IP rights.
- Choosing the appropriate OSS license.

## Choose an OSS license

Syngenta recommends using one of the two licenses below (they are the most common and widely used):

- [MIT License](#mit-license) — permissive license.
- [GNU GPLv3 License](#gnu-gplv3-license) — copy-left license.

Talk to your team and manager about the license you want to use. If unsure, always feel free to ask the OSPO team for help.

> In some cases, you may need to choose another license (for example, hardware projects or data and media). That's totally fine.
>
> [Choose an open source license](https://choosealicense.com/) website would be a good starting point. But remember — only licenses from [OSI Approved licenses](https://opensource.org/licenses/) list are allowed. Also, it's a great idea to ask the OSPO team for help in such cases.

### MIT License

[https://choosealicense.com/licenses/mit/](https://choosealicense.com/licenses/mit/)

MIT is the [most popular](https://www.synopsys.com/blogs/software-security/top-open-source-licenses/) license used in OSS projects.

It's a short and clear permissive license. Others can use the MIT-licensed code in their projects without any restrictions.

Pros:

- MIT License helps projects to obtain wide adoption. As a result of broad adoption, you could expect more contributions back to your project.

Cons:

- Do not require others to open source derivatives of your MIT Licensed project. Others could legally use your code in their projects without contributing or open-source their projects.

#### When to choose MIT License

Best suitable for general infrastructure, frameworks, and helper libraries that could be useful for communities outside Syngenta's business interests.

For example, you created a new ORM library for PostgreSQL during work on an internal software project. This library is general and could be widely used in many projects outside Syngenta's business interests. It makes sense to open the library under MIT License. It's a win-win for everyone — the community gets a new ORM library, and we may get some contributions back.

Examples of popular MIT-licensed projects: [React](https://github.com/facebook/react), [Rails](https://github.com/rails/rails), [Babel](https://github.com/babel/babel), [turf](https://github.com/Turfjs/turf/), [ant-design](https://github.com/ant-design/ant-design/), [redux](https://github.com/reduxjs/redux).

#### When not to choose MIT License

In general, MIT License is recommended. But, for some cases, it may be the best choice to use GNU GPLv3 license.

For example, you created a mobile application that calculates the best amount of fertilizers based on soil type and crop history. This application is tightly related to Syngenta's business interests. MIT License will allow competitors to take the application, rebrand it, and sell it under their name.
Neither community nor Syngenta will benefit from such a situation. It would be best if you choose a more restrictive OSS license as GNU GPLv3.

### GNU GPLv3 License

[https://choosealicense.com/licenses/gpl-3.0/](https://choosealicense.com/licenses/gpl-3.0/)

GNU GPLv3 License requires that derivative works **must** be published under the same GNU GPLv3 License. That is, the code can't later become a closed source.

GNU GPLv3 License should be used carefully. Once your code is published under GNU GPLv3 it may be impossible for Syngenta to use it in closed-source projects.

GNU GPLv3 may be reasonable for open-sourcing desktop applications or mobile apps. But not recommended for libraries and frameworks.

Pros:

- Any further development and derivatives of your project will have to be open-sourced and available to the community.

Cons:

- Generally speaking, GNU GPLv3 license is incompatible with closed-source projects or projects published under permissive licenses such as MIT License. Many others would avoid using your code in their projects. Adoption would be limited (because it's required to distribute the complete source code of your project if any library with such a non-permissive license is used in your project).

#### When to choose GNU GPLv3

Best suitable for applications, R&D, and Scientific projects.

For example, you created a desktop application that calculates the best amount of fertilizers based on soil type and crop history. This application is tightly related to Syngenta's business interests. GNU GPLv3 License will restrict competitors from taking the application, rebranding it, and selling it under their name.
However, the community and competitors are allowed to improve the application, keeping all the code open source. That will benefit both the community and Syngenta.

Examples of popular GNU GPLv3 licensed projects: [Ansible](https://github.com/ansible/ansible), [Bash](https://git.savannah.gnu.org/cgit/bash.git), [GIMP](https://gitlab.gnome.org/GNOME/gimp/), [DeepFaceLab](https://github.com/iperov/DeepFaceLab), [Signal-iOS](https://github.com/signalapp/Signal-iOS).

#### When not to choose GNU GPLv3

Not a good choice for libraries and frameworks.

For example, you created a new ORM library for PostgreSQL during work on an internal software project. This library is general and could be widely used in many projects outside Syngenta's business interests. Publishing the library under GNU GPLv3 License may restrict a significant part of the community (including Syngenta) from using the library in their closed-source or MIT-licensed projects due to the restrictive license.
The library will not get traction in the community. So, it would be best if you choose a permissive OSS license as MIT License in this case.

## Checklist

Before making the code public you should complete the checklist.

The checklist should be completed by the person who authored the code, or by the manager or team leader responsible for the development of the code. The checklist then should be signed by the appropriate R&D or IT leader.

The signing manager should be at the function manager level, as this is the level used in the scientific publication process.

Each item on the checklist should be checked and verified and ticked if true. If in any doubt, particularly about IP ownership, consult your line manager and OSPO team.

| Criteria |  |
|---|---|
| **Basic principles** |  |
| The release of the code will not be to Syngenta’s competitive disadvantage or detriment to Syngenta’s business goals. | ☐ |
| **OSS License** |  |
| Appropriate OSS license chosen. _Usually, it should be MIT or GNU GPLv3._ | ☐ |
| **IP rights and licenses compatibility** |  |
| Syngenta is able to release the Source Code as open source accordingly to chosen OSS license. We don't infringing any other parties' license or IP rights.<br>That is:<br>a) The IP rights for the code resides with Syngenta. This is likely to be the case for code written by 3rd party companies on behalf of, and paid by, Syngenta. The same generally applies to code written by Syngenta employees. For students/temporary/contract staff the terms of their contract should be checked. If in any doubt, please consult your line manager and, if needed with the OSPO team. | ☐ |
| AND<br>b) Any portion of the code that was not created in-house has been provided and licensed to Syngenta in a manner that allows us to release it as part of our project under chosen OSS license. Please note that even if the code was commissioned by Syngenta, this does not automatically mean that we own all of the IP rights in the code. If in any doubt, please please consult your line manager and, if needed with the OSPO team. | ☐ |
| AND<br>c) No code is included that was provided and licensed to Syngenta under a commercial licence (however the code was obtained). You should always check the terms of the latest version of the licence which applies to the code. | ☐ |
| **Publishing** |  |
| Source code will be published accordingly to chosen OSS license standards and requirements, respecting licenses of all included 3-rd part code.<br>For example: keeping copyright notices, full text of license, full text of licenses of all included OSS libraies.  | ☐ |
| **Additional** (if applicable) |  |
| Publishing of the code has been agreed with scientific community. | ☐ |
| **Done** | |
| Checklist Completed By:<br> Date: |  |
| Approved By:<br>Date: | |

## Publishing to GitHub

By default, we publish all Syngenta's open-source projects under the [Syngenta GitHub organization](https://github.com/syngenta/). It's also OK to publish your code to other platforms (for example, [Zenodo](https://zenodo.org/)).

The OSPO team will help you to create a new repository in Syngenta's GitHub organization and to publish the code. In general, the steps look like this:

1. The OSPO team creates a new **private** repository in Syngenta's GitHub organization and adds users and teams to the repository.
2. Preparing your code for publishing:
    - Ensure there is a detailed `README` (or `README.md`, `README.rst`) [readme file](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) describing the project:
      - what the project does;
      - why the project is useful;
      - how users can get started with the project;
      - where users can get help with your project;
      - who maintains and contributes to the project.
    - Remove any sensitive data from the code (API Keys, etc.).
    - Consider squashing existing commits to keep the history clean and avoid leaking private data that could be present somewhere in commit history.
    - Ensure you have a proper `LICENSE` or `COPYING` file in the repository, accordingly to chosen OSS license.
    - For the MIT License, check that the `LICENSE` file contains the following copyright notice: `Copyright <YEAR> Syngenta Group Co. Ltd.` (replace `<YEAR>` with the year of release). No need to add a copyright notice to the beginning of each source file.
    - For the GNU GPLv3 License, it's recommended to [add copyright notices to each source file](#how-to-apply-gnu-gplv3-terms-to-the-new-software).
    - [Additional recommendations](basic-github-code-publishing-and-settings-recommendations.md).
3. The OSPO team pushes the code to the new repository.
4. The OSPO team makes a general look over your code to ensure it is ready for publishing:
    - general look over your code and propose help with areas we have experience with (e.g., best practices, automation, code quality, marketing);
    - check the chosen license;
    - help ensure that some secret/private API tokens are not present in code or git history.
5. The OSPO team makes the repository **public** 🎉.

These steps may be different for each particular case. Feel free to contact the OSPO team for help — we will manage the best path.

## Appendix

### How to apply MIT License terms to the new software

Add the following `LICENSE` file to the root of the repository:

    The MIT License (MIT)

    Copyright <YEAR> <COPYRIGHT HOLDER>

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

- `<YEAR>` must be replaced with a year of release.
- `<COPYRIGHT HOLDER>` must be replaced with: `Syngenta Group Co. Ltd.`.

Adding the copyright notice to the source code files is not required.

### How to apply GNU GPLv3 terms to the new software

1. Add the `COPYING` file to the root of the repository with the full content of the license [https://www.gnu.org/licenses/gpl-3.0.txt](https://www.gnu.org/licenses/gpl-3.0.txt).
1. It's recommended to add the copyright notice to the source code files.

From the official GNU GPLv3 license text:
> If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these
terms.
>
>To do so, attach the following notices to the program. It is safest to
attach them to the start of each source file to most effectively state
the exclusion of warranty; and each file should have at least the
"copyright" line and a pointer to where the full notice is found.
>
>     <one line to give the program's name and a brief idea of what it does.>
>     Copyright (C) <year>  <name of author>
>
>     This program is free software: you can redistribute it and/or modify
>     it under the terms of the GNU General Public License as published by
>     the Free Software Foundation, either version 3 of the License, or
>     (at your option) any later version.
>
>     This program is distributed in the hope that it will be useful,
>     but WITHOUT ANY WARRANTY; without even the implied warranty of
>     MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
>     GNU General Public License for more details.
>
>     You should have received a copy of the GNU General Public License
>     along with this program.  If not, see <https://www.gnu.org/licenses/>.
>
> Also add information on how to contact you by electronic and paper
mail.
>
> If the program does terminal interaction, make it output a short
notice like this when it starts in an interactive mode:
>
>     <program>  Copyright (C) <year>  <name of author>
>     This program comes with ABSOLUTELY NO WARRANTY; for details type `show w'.
>     This is free software, and you are welcome to redistribute it
>     under certain conditions; type `show c' for details.
>
> The hypothetical commands \`show w' and \`show c' should show the
appropriate parts of the General Public License. Of course, your
program's commands might be different; for a GUI interface, you would
use an "about box".
>

- `<year>` must be replaced with a year of release.
- `<name of author>` must be replaced with: `Syngenta Group Co. Ltd.`.
