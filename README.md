# CPSC

A site for anyone learning or getting into Computer Science to get started and learn useful development techniques and utilities.

The goal of this project and site is not to just copy and paste guides from all over the internet, but to synthesis information and centralize the basics of topics. I have often found that once I learn and get invested in a tool or idea, it is a lot easier for me to continue learning, exploring, and using it. This project's purpose is to be that spark as well as being a showcase of common tools and workflows.

![Netlify](https://img.shields.io/netlify/53402166-eddd-4b58-8275-2e6ca7c2c1ce?label=dev%20builds&logo=netlify&style=plastic)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/jhollowe/cpsc/Deploy%20to%20gh-pages%20branch?logo=github&style=plastic)
![GitHub last pages build](https://img.shields.io/github/last-commit/jhollowe/cpsc/gh-pages?label=latest%20build)

![GitHub contributors](https://img.shields.io/github/contributors/jhollowe/cpsc?color=green)
![GitHub stars](https://img.shields.io/github/stars/jhollowe/cpsc?style=social)

## Contributing

Please read the [Contributing Guidelines](CONTRIBUTING.md)

## Development

The main dependency for development is Hugo. You can download the latest [Hugo release](https://github.com/gohugoio/hugo/releases/) or use your package manager of choice, just be sure to get the **extended version** to allow for compiling the SASS to CSS. You can also follow the [official install guide](https://gohugo.io/getting-started/installing).

#### Clone Repo

- `git clone --recursive https://github.com/jhollowe/cpsc.git`
  - The `--recursive` is important to also clone the theme's submodule repo
- `cd cpsc`

#### Build Site

This builds the site one time into the `public/` directory.

- `hugo` OR
- `hugo --minify`
- (run `hugo help` for more options)

#### Live Test Site

This serves the site, watches for file changes, and updates the served content to be the latest changes on disk.

- `hugo server` OR
- `hugo server --minify`
- (run `hugo help` for more options)
