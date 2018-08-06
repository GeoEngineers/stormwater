## Industrial Stormwater Communities of Interest Website Builder

This repo contains source code for generating a static website for the Industrial Stormwater Communities of Interest organization.

The website consists of static HTML and assets generated using a build tool called [Jekyll](https://jekyllrb.com/).

Jekyll takes static assets such as Markdown files, HTML templates, CSS and images and generates a ready-to-deploy static website.

### Getting started

To get started, clone this repo locally using [git](https://git-scm.com/):

```
git clone https://github.com/GeoEngineers/stormwater.git
```

Jekyll requires Ruby to be installed first. (If you don't have ruby installed, follow the [instructions on the Ruby website](https://www.ruby-lang.org/en/downloads/).) Then you can install Jekyll with the following command:

```
cd stormwater
jekyll server --watch
```

This will launch the Jekyll server and host a development version of the website on your local computer, which can be accessed in a browser at `http://localhost:4000`.

To make changes, open `index.md` or the `.md` files located in the `pages` folder. The Jekyll process will automatically update the preview site in your browser.

### Using Markdown files

[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight and fairly standard way to write text for the web without having to write full HTML. It takes simple notation and converts it to HTML using a processing tool. Support for that conversion is built right into Jekyll. Here's an excellent cheatsheet for the Markdown syntax: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet. This style of formatting is probably not the WYSIWYG text editing that you are used to, but is a way to indicate standard _semantic_ formatting, such as headers, bold text, italics, unordered lists, etc. The fonts, sizes, colors, etc. are controlled using a CSS file that applies to the entire website. This keeps the _meaning_ of the text and the _display_ of the text nicely separated.

### Templates

The HTML templates used to build the pages are located in the `_layouts` and `_includes` folders. Layouts are whole pages, whereas includes are smaller chunks of pages. See the [Jekyll documentation for a full rundown of how Jekyll works](https://jekyllrb.com/docs/home/).

### Building for deployment

Running the `server` command is a convenience tool for development purposes. To build the final HTML and associated assets for deployment, run the build command:

```
jekyll build
```

This will create a production-ready bundle located in the `_site` folder. This folder can then be uploaded to a web server.

### Use with Github Pages

Github has built-in Jekyll integration. If you update the source `.md` files, commit the changes, and push your changes to Github, the site will generate the bundled site automatically _on the Github-hosted version of the site_, that is https://geoengineers.github.io/stormwater/. For more information on the Github Flow, see the [Github Guides page](https://guides.github.com/).

The Github Pages hosted version of the site (http://geoengineers.github.io/stormwater) is useful for sharing a development version of the sight with other collaborators before deploying an official build to a permanent hosting location.
