# Report

Northwestern University Libraries was awarded a grant from [the Association of Research Libraries Venture Fund](https://www.arl.org/news/arl-launches-venture-fund-to-support-research-and-development-in-member-libraries-proposals-due-february-28/) to develop a digital publishing toolkit for librarians who support open educational resources (OER) publishing on their campuses. This report documents the outcomes and future for our project, which we've named *Lantern*, available here: <https://github.com/nulib-oer/lantern>

Lantern is prototype that applies *minimal computing* principles to the production, hosting, and maintenance of OER. At its core, Lantern is a script, template, and documentation that makes it easier to use [Pandoc](http://pandoc.org/) and [GitHub](https://github.com/) to produce and distribute open textbooks in multiple formats, such as HTML, PDF, EPUB, and DOCX. Lantern produces OER content in formats that make it easier to publish, preserve, and reuse by students, faculty, and librarians.

## Why did we create Lantern? 

OER programs at academic libraries typically license a publishing platform from a vendor or develop their own with open source software. Most publishing platforms are maintained by product managers, software developers, and other professionals who are responsible for writing documentation, adding features, patching security vulnerabilities, and updating software dependencies. This is costly to sustain and creates a risk for [vendor lock-in](https://en.wikipedia.org/wiki/Vendor_lock-in).

Lantern approaches this problem in the following ways:

-   **Minimal technology stack:** Lantern was designed to use the fewest amount of software dependencies possible. Each dependency is cross-platform open source software that can run on any machine.

-   **Multiformat static outputs:** Lantern generates static HTML, PDF, EPUB, and DOCX files that can be distributed by web hosting service without setting up any databases, server-side application software, or content management systems. These files can also be added to preservation systems in compressed or uncompressed formats.

-   **Non-proprietary:** Lantern teaches the value of non-proprietary plain text documents for accessibility and preservation.

-   **Portability:** Lantern can be used the web, in the form of a GitHub repository, or as part of a standalone production environment, where users can install and run the required programs on their own. 

-   **Free:** Lantern is distributed for free and under an open license. The first edition of Lantern is available on GitHub and assumes that the user has created a free GitHub account, but Lantern itself can be [downloaded as a .zip file](https://github.com/nulib-oer/lantern/archive/refs/heads/main.zip) and used without a GitHub account by anyone.

-   **Transferable skills:** We make no promises that Lantern will be available and usable forever. We do, however, believe that the skills and knowledge introduced in Lantern's workflow are applicable to a variety of web and digital projects.

With Lantern, we hope to demystify a few developer tools (text editors, GitHub, and open-source software) for beginners interested in digital publishing by connecting these technologies to concepts, such as metadata, preservation, and information accessibility.

## Enduring and Barrier-free Access to Information

Lantern was inspired by *minimal computing*. Minimal computing refers to "computing done under some set of significant constraints of hardware, software, education, network capacity, power, or other factors" [@noauthor_what_nodate]. For Lantern, we decided to set constraints on our technology choices to minimize costs and technical obsolescence for the preservation and dissemination of digital, educational materials.

Lantern's emphasis on multiformat static outputs, non-proprietary file formats, portability, and free-of-charge software are intended to support ARL's commitment to enduring and barrier-free access to information. Markdown is an excellent choice for this goal. We use it as the source format from which we can generate PDF, HTML, and EPUB versions of the OER. Here is an example of Markdown source code:

```
Introductory paragraph text with **bold** and *italic* text.

## Section Heading

Introductory paragraph for the section.

Another paragraph, but with a [link to a website](https://example.com).

### Subsection HeadingMore content, but in list form:

- list item
- list item
- list item
```

> The idea is to identify logical structures in your document (a title, sections, subsections, footnotes, etc.), mark them with some unobtrusive characters, and then "compile" the resulting text with a typesetting interpreter which will format the document consistently, according to a specified style. ---[@tenen_sustainable_2014]

[Lantern\'s documentation](https://github.com/nulib-oer/lantern/wiki) walks users through the conversion and Markdown typesetting process. The basic workflow can be completed entirely online, using only a web browser and free a GitHub.com account. No installation of any software is required. Most users go from manuscript to published OER in an hour.

While the basic workflow relies on GitHub to perform most of the processing and hosting work, Lantern can be downloaded and used on any operating system, removing GitHub as a dependency. Users who opt to run Lantern on their own machines will have to install some software on their own. Publishing the OER without GitHub requires access to a basic web hosting service. Since Lantern produces static HTML, there are numerous free hosting options available, such as [Amazon Web Services (free tier)](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all) and [Netlify](https://app.netlify.com/drop).

Upon completing an OER project with Lantern, users will have the files for a website, PDF, EPUB, DOCX, and a source directory of plain text files for dissemination and preservation of the content.

## Librarian Review Panel

We wanted to make sure that Lantern, as an idea, was worth developing further. We assembled a panel of six librarians at academic libraries around the country to test and review an early version of Lantern. Each librarian was paid a stipend to review the documentation, complete two tutorials, and discuss their experiences. Some quotes from our interviews:

> \"You\'ve provided an environment in which librarians who are not programmers could experiment with using markdown. There\'s a lot that\'s unfamiliar, and I feel like what you\'ve done is to make it more accessible to people like me.\" -- Anita Walz, Assistant Director of Open Education, Virginia Tech University Libraries
>
> "With Lantern, OER creation is made very simple. I could follow along and actually get a textbook produced." -Kathy Clark, Director, Phillips Library, Aurora University
>
> "With Lantern, you can take files that someone gives you and create a website without having to do anything, really. I could take a 300-page Word document textbook and easily turn it into a website.\" -Tim Fluhr, Head of Library Services, Illinois Institute of Technology

This process generated numerous great ideas, resulting in a major overhaul of the original documentation and workflow. For this iteration of _Lantern_, we provide documentation for the "GitHub workflow" and minimal guidance on the "Desktop workflow" (i.e. standalone environment, _without_ GitHub). Future iterations will provide more helpful instruction on using Lantern in a stanadlone production environment on the user's computer. 

## Deliverables

We produced the following items with ARL grant support:

-   [GitHub repository template](https://github.com/nulib-oer/lantern) for creating and publishing an OER textbook
-   [Documentation](https://github.com/nulib-oer/lantern/wiki/) containing instructions, guides, and recommended resources
-   Extensible [templates](https://github.com/nulib-oer/lantern/tree/main/templates) for HTML, PDF, and EPUB output formats
-   [Scripts](https://github.com/nulib-oer/lantern/blob/main/lantern.sh) for converting from Microsoft Word to Markdown and Markdown to various output formats

In addition to the above, our work involved:

-   The creation of Lantern user personas
-   In-depth user testing and interviews with six librarians
-   An accessibility audit of the project website and output templates
-   Creation of a logo and custom book cover templates

## Scalability

Lantern is designed to be a template for using [Pandoc](https://pandoc.org/) as a publishing tool. Pandoc is a popular document converter that can handle dozens of file formats. While powerful, Pandoc can be challenging to learn without a strong familiarity with command line programs and markup languages (like HTML). Lantern provides the fundamentals (instructions, explanations, and templates) from which users can explore numerous customizations for their projects. Our hope is that Lantern can be used as-is for open textbook projects, but also be modified for a variety of text-based digital web projects.

We have ideas on how Lantern could be used by content creators beyond the open textbook paradigm. While the primary audience is currently librarians and the primary output is OER, Lantern's methods could be used to easily turn meeting notes, slide decks, conference proceedings, presentations, personal writing projects and more into static websites and PDFs. In other words, we can see how the variety of use cases could expand Lantern's use beyond its original intention.

## Sustainability

We have just started using Lantern on OER projects at Northwestern University, so it is too soon to tell if Lantern as a software is sustainable. We, personally, are committed to using and maintaining Lantern on Northwestern OER projects for as long as Lantern meets the needs of our OER authors.

We are confident, however, that the publication outputs produced by Lantern can be sustained in terms of access and preservation by libraries. Lantern outputs produce multiple formats (Markdown, HTML, PDF, EPUB, and DOCX) as static files. The flexibility of multiple, non-proprietary output formats gives librarians some assurances future software will be able to read and compile the files for later use.

## Future

We have three priorities for Lantern: (1) use Lantern to publish OER textbooks by Northwestern University authors, (2) extend Lantern to support more use cases, and (3) promote Lantern at academic librarian conferences.

First, we are currently using Lantern on OER projects Northwestern University Libraries supports, developing and releasing new features as needed (such as full-text search). We began by migrating two OER projects from [Bookdown](https://bookdown.org/) to Lantern[^1]: [***Empirical Methods in Political Science: An Introduction***](https://emps.northwestern.pub/) by Jean Clipperton and ***Introduction to Material Science and Engineering*** by Kenneth Shull, Jonathan Emery, and Jacob Kelter.

Second, we were thrilled to discover new use cases for Lantern from the Librarian Review Panel interviews, including:

-   *Convert LaTeX to EPUB:* LaTeX is a popular typesetting language for STEM disciplines, but PDFs generated from LaTeX are not accessible. EPUB, however, is a more accessible format than LaTeX and PDF. Lantern could be extended to support a workflow that generates EPUB from LaTeX source.

-   *Create a public website from a Google Doc:* Google Docs are powerful tools for collaboratively generating a document from a learning activity. Instructors might want to generate a more stable and sharable version of the Google Doc by converting it into a static website. Google Docs can export to .DOCX or .ODT formats, which Lantern can convert to Markdown, then HTML.

Third, we will be promoting Lantern at several academic librarian conferences in the spring and summer of 2022. We hope to connect with potential users on GitHub. Lantern users who have questions can use the [discussion forum](https://github.com/nulib-oer/lantern/discussions) or [issue tracker](https://github.com/nulib-oer/lantern/issues) to report a bug or request a feature.

We believe that Lantern is aligned with the movement working toward [an open infrastructure for scholarly communication](https://investinopen.org/about/) and has the potential to be an important option for [open source publishing tools](https://mindthegap.pubpub.org/). We hope Lantern can provide an on-ramp to more librarians interested in applying minimal computing techniques to open education initiatives.

[^1]: Bookdown is a major influence for the development of Lantern. We strongly recommend Bookdown to any users who are familiar with the R programming language. We developed Lantern as an alternative to Bookdown in order to provide a similar option to user who are unfamiliar with the R programming language (and therefore do not need the features Bookdown provides to R users).