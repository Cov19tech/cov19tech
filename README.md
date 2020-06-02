## About this Repository
This repository contains the source code and content for [Cov19Tech.org](https://Cov19Tech.org). Cov19Tech is an open effort to document and share information on emerging technology being built to aid in stopping the spread of COVID-19. Cov19Tech focusses primarily on software & mobile technology, such as contact tracing apps, rather than life sciences technology (therpauetics, diagnostics, vaccines) being developed. 

The initial focus on Cov19Tech is to document the array of contact tracing applications being released by national and local governments worldwide. The information collected on these apps is intended to give a thorough overview of the approaches and tradeoffs. Although the information is intended for a technical audience, we are attempting to make it as accessible as possible to a broad range of interested parties.

## Development
The site is built with [Hugo](https://gohugo.io/]) with the [LoveIt theme](https://themes.gohugo.io/loveit/). 

As is the Hugo standard, the content for the site is under the */content* folder. Data for the summary table on the main site is in the */data* folder. 

To build this site, clone this repository and make sure you have Hugo installed.

You can then build the site with

```bash
  hugo -D
```
After a successful build, you'll have a new folder public in the repository's base directory. It contains the generated files for the complete website

For development, you can use
```bash
  hugo server -D
```
which will make the site available for testing at http://localhost:1313/

We welcome any pull requests.

## Support and Feedback
For discussion, issues, and bugs, you can use the [issues section of this repostory](https://github.com/Cov19tech/cov19tech/issues)
For other requests, please use the [contact page on Cov19Tech](https://cov19tech.org/contact)

## License
The source code for this site is licensed under Apache License, Version 2.0

The content on the website is licensed under the [Creative Commons CC BY 4.0 license](https://creativecommons.org/licenses/by/4.0/)
