# TEPEI.org

Welcome to the Github repo for Tau Epsilon Phi - Epsilon Iota's public-facing homepage! Visitors will find information about the current semester's Rush and the brotherhood in general.

If you're the EI Chapter's current House Computing chairman, your responsibilities are as follows:
- Make sure event information for Rush is up to date (dates, what each event is)
- Coordinate with the Historian to make sure this website is populated with nice pictures! Bonus points if you set up an archive with older ones (not from tepstagram)

## Development

1. Clone this repository
2. Install [Ruby](https://www.ruby-lang.org/en/downloads/)
3. Install build dependencies: `gem install jekyll bundler`
4. Install theme-specific dependencies: `bundle install`
5. Build and locally serve the website: `bundle exec jekyll serve`
6. Open [http://localhost:4000](http://localhost:4000) in your development browser

Once you're satisfied with your changes:

1. Commit and push them
2. Build the website: `bundle exec jekyll build`

The built website will live in `_site/`. If the previous House Computing chair doesn't want you or the chapter to suffer, he'll have given you the FTP credentials.

TODO: Continuous integration (automatically update http://tepei.org whenever the contents of this repo change)

## Structure/Layout

The current TEPsite is built with [Jekyll](https://jekyllrb.com/docs/home/), a Ruby gem optimized for blogging which allows you to create HTML elements using Markdown. Do yourself a favor and at least skim the documentation before you start making changes.

Jekyll assembles a static website based on HTML partials, which are contained in `_includes/`.

**Important notes**:
- The three pages linked from the homepage (Rush, About, and Brothers) are technically blog posts instead of their own static pages. It's nice to have a copy of old Rush materials, so whenever a new semester's Rush begins, duplicate the Rush page and change it in order to publish new information, and move the old copy to `archive/`.
- The order in which these three pages are displayed depends on the hyphenated date in their respective Markdown filename. Make sure Rush comes first!

### Configuration

Global site settings are in `_config.yml` in YAML format, which is basically JSON but nesting is indicated with indentation.

Information in this file includes:
- search engine optimization (social media links)
- how to structure permalinks to various pages

Information about active brothers resides in `_data/brothers.yml`. This currently includes names and E-Board positions.

### Front matter

[The Jekyll docs](https://jekyllrb.com/docs/frontmatter/) contain the simplest explanation of what front matter is and how it works. Basically it's YML information at the top of every page/post Markdown file that includes helpful meta-information, like page titles and post dates.

[The theme docs](https://github.com/thomasvaeth/trophy-jekyll#_posts) indicate which particular front matter variables are useful for you (page titles, SEO images, etc.).

## Theme

Andrew chose the [Trophy](https://github.com/thomasvaeth/trophy-jekyll) Jekyll theme for its clean a e s t h e t i c. You can change it if you want, but it'll be a pain in the ass if you're not familiar with Jekyll already.

### Styling

Styles are in `_sass/`. Most of the custom stuff (e.g. colors, fonts, styling for the Brothers page) is in `_sass/_base.scss` and `_sass/_layout.scss`.