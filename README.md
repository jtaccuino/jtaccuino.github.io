# JTaccuino website

Build state:
![GitHub Actions build state](https://github.com/jtaccuino/jtaccuino.github.io/workflows/hugo%20publish/badge.svg)

Sources of [the documentation website of the JTaccuino project](https://jtaccuino.github.io/).

## Contribute 

If you want to contribute to this website, make a fork and create a merge request.

## Created with GoHugo

This website is created with the static site generator [Hugo](https://gohugo.io/).

### Theme

Uses the [Hugo-theme-learn](https://learn.netlify.app/en/).

Special layout components are explained on [learn.netlify.app/en/shortcodes](https://learn.netlify.app/en/shortcodes/notice/).

### Text format

All pages are separate md-files inside the [content](content/) directory. The formatting
of the text needs to use the rules specified in [commonmark.org](https://spec.commonmark.org/0.29/).

Notes can be included like this:

```
{{% notice note %}}
Some text
{{% /notice %}}
```

Available types:

* `notice note`: blue box
* `notice tip`: green box
* `notice warning`: red box

Example:

```
{{% notice tip %}}
Some text
{{% /notice %}}
```

### Images

#### Location for images

Upload new images to `/static/assets/`.

#### Single image 

To include a single image in your content use the following structure:

`![DESCRIPTION](/assets/DIR/FILE)`

### Test locally

To test the site locally, first install Hugo as described on ["Install Hugo"](https://gohugo.io/getting-started/installing/).

Example, for Mac:

```
brew install hugo
```

To run the site, open the terminal in the directory with the sources of this site and run the following command:

```
cd jtaccuino.github.io
hugo serve
```

The website is now available on [localhost:1313](http://localhost:1313/).

### Build and run on GitHub Pages

Using a GitHub Action, the site is published on each commit into the main branch of this repository.

***The "docs" directory is auto-generated by this GitHub Action so should never be manually touched. This directory is pushed to GitHub Pages.***

This process is described here:

* [Automate your GitHub Pages Deployment using Hugo and Actions](https://medium.com/@asishrs/automate-your-github-pages-deployment-using-hugo-and-actions-518b959a51f9)
* [Deploy Hugo project to GitHub Pages with GitHub Actions](https://discourse.gohugo.io/t/deploy-hugo-project-to-github-pages-with-github-actions/20725)
