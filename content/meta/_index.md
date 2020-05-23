---
title: "Creating This Site"
date: 2020-05-03T20:52:31Z
draft: false

weight: 999
---

This section is devoted to recording and explaining the steps taken to create this site. It's also a good example of contributing to a open source project.

{{<alert style="warning">}}This section discusses [Git](git/). You don't _need_ to have completed that section, but it might help. {{</alert>}}

### Major Components

This site is created using [Hugo](https://gohugo.io/), A static site building utility. The site is automatically built using [GitHub Actions](https://github.com/features/actions)
and is hosted on [GitHub Pages](https://pages.github.com/). I'm using the [Ace documentation](https://github.com/vantagedesign/ace-documentation) theme for Hugo with a few customizations
and tweaks.

### Design Choices

I specifically wanted to use a workflow that I can make as transparent as possible. This includes all the [source material for this site being public](https://github.com/jhollowe/cpsc) and
using a simple source material format (Markdown) that is built into a final page. This allows for easy contributions and central management of the site's style and format.

I also didn't want to have to host the site on my own server or place it on a free-to-me server that is access restricted or ephemeral (Clemson's CS servers). I also wanted contributions to
the project to be easy. These factors came together to use GitHub for the source repository and GitHub pages for the hosting. GitLab pages have more native and easier integration with Hugo
building, but GitHub is where the community is. I could set up mirroring of the repo between GitHub and GitLab, but I felt that this would cause confusion and a hinderance to new contributors
knowing how to contribute or ask questions.

I also didn't really feel like creating a site from scratch. Bootstrap is a great boost (thus "_bootstrap_"), but being able to just import a theme into a site build tool was very convenient
and has probably handled more edge cases and oddities that I could think of or find. I also don't have great stylistic abilities, so a known-good is always nice.
