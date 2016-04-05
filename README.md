# UnConference Canberra Jekyll website

## Introduction

This git repo holds the content, templates, etc. for [the unCon Canberra website](http://unconferencecanberra.org).

The data held here is the input given to [Jekyll](https://jekyllrb.com/), a static-site generator.

A static-site generator takes plaintext content, layouts, and stylesheets, parses them, and spits out static HTML/CSS/JS on the other end. This output is then copied over onto the web server running unconferencecanberra.org. This process is enacted automatically every time a new git *commit* is made to the `master` (default) branch of this repository.

So, in other words: if you push a change to this repository it will take your edits, rebuild the files that comprise the site, and (re)deploy it to the live web server.

## Editing --- getting started

All you need in order to edit the website is a GitHub account, associated with contributor rights to this repository. (Ask klepas or maxious if you need rights.)

You can download the repository to your local computer (git clone) using the GitHub app for your platform, or you can edit the site’s content on GitHub.com directly, using their web interface. This is the easiest method.

1. Navigate to the file you wish to edit (e.g. the [*What to expect* markdown file](https://github.com/unconferenceCanberra/unconfcbr-website/blob/master/expectations.md));
2. Click the pencil “Edit this file” icon to the right in the header for that file (right of the “Raw”, “Blame”, and “History” buttons);
3. Edit the file using [Markdown](https://en.wikipedia.org/wiki/Markdown) syntax, always leaving the metadata section at the top of the file intact (edit fields as needed);
4. Previewing edits is possible, where GitHub turns your edited Markdown into HTML (using GitHub’s internal stylesheet for now): select the “Preview changes” tab;
5. To save, scroll to the bottom and provide a summary about your changes, and then commit your changes into the `master` branch.

If you’re unsure about going live with your changes, select the second radio button (“Create a **a new** branch for this commit and start a pull request”). This will create a new fork or branch of the entire repository at that point in time, with your new changes. It also notifies others involved in the project, and allows them to review the changes to merge them back into main (default, `master`) branch.

## Finding the right file to edit

**Where is the event data, how do I change the site email address, and where are the unorganisers’ details stored?**

### Static pages

You can find these as `.md` files, e.g., the *What to expect?* page is called `expectations.md`; the *Code of Conduct* is found in `conduct.md` and so on.

The main homepage text is found inside `index.md`.

### Hero banner event info (homepage header)

Since this information changes yearly (at least the year, venue, date, etc.), and is associated to the event listing for past events, this is held inside `_data/events/`. There you will find a plain text file for each year. Follow the syntax and you'll be fine.

When it comes time to edit the information for the next event, simply create a new file (e.g. `2017.yml`) inside the `_data/events/` folder, keeping the same syntax intact and the homepage hero information will update, since it always uses the latest event file.

Note: the Eventbrite link here also provides the URL for the *Participate* links in the header and footer.

### Other links

A number of other links are declared in `_data/links.yml`, including:

- the site email address (referenced in the header and footers, and *Code of Conduct* page);
- the YouTube account;
- the Twitter account;
- the Facebook account.

If you want to edit the social media items edit the new name of the account; the URLs to, e.g., facebook.com are already included in the templates --- it's just the account names at the end of the URL strings that are missing, and supplied via this file.

### Event Google map embed

This is currently hard-coded, and is located in the `map-home.html` include, in the `_includes/` folder.

It would be cool to also tie the map location to each event (as a venue), so that the map is updated automatically based on the venue listed for that year (something to do).

### Sponsors

Currently these are not tied to each event year (something to do). Thus it's required to edit these each year.

You can find the sponsors list in `_data/sponsors.yml`. Follow the syntax as with previous entries.

The layout is currently designed to hold rectangular logos. Please consider keeping these to roughly the same dimensions, and place the logo file itself into `images/sponsors/`; the filename there needs to match what you enter into the `sponsors.yml` file.

### Unorganiser list (footer)

This is another data file, found in `_data/unorganisers.yml`. If you need to add a new unorganiser simply add them, following the existing syntax.

Regarding links: the footer text for that unorganiser will link to their website (if defined), then their twitter page (if defined), or otherwise simply their name, sans link.

## Technical setup

- Dependencies for building the site locally is are currently *unversioned*; probably should version these, or at least minor-match version them (something to do).
- Uses the [jekyll-assets](https://jekyll.github.io/jekyll-assets/) plugin for an asset pipeline.
- Uses the [bourbon.io](http://bourbon.io/) SASS mixin library and it’s grid framework [neat.bourbon.io](http://neat.bourbon.io/). Note that these might not be perfectly included and referenced in the `_assets/` folder.
- Template logic is held inside `_layouts/`, with commonly reused elements (like header and footer) in `_icludes/`.
- Details about unorganisers, the site email contact address, and event details are stored in metadata files in `_data/`.
- Uses *Merriweather* and *Source Sans Pro* from Google Web Fonts, and Font-Awesome for icons.

## License

Bourbon and Neat are licensed under the MIT License by thoughtbot, inc.

The remaining texts-based works here are also licensed under the MIT License. See LICENSE.md.

Photos included in the website are licensed separately, as noted on the pages where they are used.
