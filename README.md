# UnConference Canberra Jekyll website

## Introduction

This git repo holds the content, templates, etc. for [the unCon Canberra website](http://unconferencecanberra.org).

The data held here is the input given to [Jekyll](https://jekyllrb.com/), a static-site generator.

A static-site generator takes plaintext content, layouts, and stylesheets, parses them, and spits out static HTML/CSS/JS on the other end. This output is then copied over onto the web server running unconferencecanberra.org. This process is enacted automatically every time a new git *commit* is made to the `master` (default) branch of this repository.

So, in other words: if you push a change to this repository it will take your edits, rebuild the files that comprise the site, and (re)deploy it to the live web server.

## Editing -- getting started

All you need in order to edit the website is a GitHub account, associated with contributor rights to this repository. (Ask klepas or maxious if you need rights.)

You can download the repository to your local computer (git clone) using the GitHub app for your platform, or you can edit the site’s content on GitHub.com directly, using their web interface. This is the easiest method.

1. Navigate to the file you wish to edit (e.g. the [*What to expect* markdown file](https://github.com/unconferenceCanberra/unconfcbr-website/blob/master/expectations.md));
2. Click the pencil “Edit this file” icon to the right in the header for that file (right of the “Raw”, “Blame”, and “History” buttons);
3. Edit the file using [Markdown](https://en.wikipedia.org/wiki/Markdown) syntax, always leaving the metadata section at the top of the file intact (edit fields as needed);
4. Previewing edits is possible, where GitHub turns your edited Markdown into HTML (using GitHub’s internal stylesheet for now): select the “Preview changes” tab;
5. To save, scroll to the bottom and provide a summary about your changes, and then commit your changes into the `master` branch.

If you’re unsure about going live with your changes, select the second radio button (“Create a **a new** branch for this commit and start a pull request”). This will create a new fork or branch of the entire repository at that point in time, with your new changes. It also notifies others involved in the project, and allows them to review the changes to merge them back into main (default, `master`) branch.

**Where is the event data, how do I change the site email address, and where are the unorganisers’ details stored?**

A range of information is stored separately inside metadata `.yml` files. You can find these inside the `_data/` folder. The formatting should be fairly apparent; if you need to make a new entry (e.g. adding a new unorganiser) follow the formatting used by the previous entries.

## Setup info

- Content is placed directly into plaintext `.md` markdown files.
- Template logic is held inside `_layouts/`, with commonly reused elements (like header and footer) in `_includes/`.
- Details about unorganisers, the site email contact address, and event details are stored in metadata files in `_data/`.
- Uses *Merriweather* and *Source Sans Pro* from Google Web Fonts, and Font-Awesome for icons.
- Uses the [jekyll-assets](https://jekyll.github.io/jekyll-assets/) plugin for an asset pipeline.
- Uses the [bourbon.io](http://bourbon.io/) SASS mixin library and it’s grid framework [neat.bourbon.io](http://neat.bourbon.io/)

## License

Bourbon and Neat are licensed under the MIT License by thoughtbot, inc.

The remaining texts-based works here are also licensed under the MIT License. See LICENSE.md.

Photos included in the website are licensed separately.
