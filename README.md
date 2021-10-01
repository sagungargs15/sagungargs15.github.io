# sagungarg.com - Personal Website of Sagun Garg
This repository is representing the source code of my private website https://sagungarg.com that is hosted with GitHub Pages. The website is powered by Jekyll and I can use Markdown to author my posts. It is inspired from  multiple themes and source codes
    - [Minimalist](https://github.com/BDHU/minimalist). 
    - [Jonathan McGlone’s](https://github.com/hankquinlan/hankquinlan.github.io/) project. ![Demo of Minimalist](https://raw.githubusercontent.com/BDHU/minimalist/main/minimalist.png)
    

This project on purpose does not provide a license. That means it is under my exclusive copyright.
The reason for that being that 99% of this repo is private data of myself.

Therefore I would recommend to use [Jonathan McGlone’s](https://github.com/hankquinlan/hankquinlan.github.io/) project as a starter, since it doesn't contain any private information and the author allows copying without restrictions.

## Instructions
GitHub Pages builds automatically on commits. Files can directly be edited within the GitHub UI.

### Local development:
`jekyll serve` builds and serves the page at [http://localhost:4000](http://localhost:4000)

See also [Jekyll docs](https://jekyllrb.com/docs/usage/)


# The Minimalist theme

*Minimalist is a Jekyll theme, inspired by the . You can [preview the theme to see what it looks like](http://bdhu.github.io/minimalist), or even [use it today](#usage).*



## Usage

To use the Minimalist theme:

1. Add the following to your site's `_config.yml`:

    ```yml
    remote_theme: BDHU/minimalist@v0.1.0
    plugins:
    - jekyll-remote-theme # add this line to the plugins list if you already have one
    ```

2. Optionally, if you'd like to preview your site on your computer, add the following to your site's `Gemfile`:

    ```ruby
    gem "github-pages", group: :jekyll_plugins
    ```

## Customizing

### Configuration variables

Minimal will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
google_analytics: [Your Google Analytics tracking ID]
```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:

    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```

3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

### Layouts

If you'd like to change the theme's HTML layout:

1. For some changes such as a custom `favicon`, you can add custom files in your local `_includes` folder. The files [provided with the theme](https://github.com/BDHU/minimalist/tree/master/_includes) provide a starting point and are included by the [original layout template](https://github.com/BDHU/minimalist/blob/master/_layouts/default.html).
2. For more extensive changes, [copy the original template](https://github.com/BDHU/minimalist/blob/master/_layouts/default.html) from the theme's repository<br/>(*Pro-tip: click "raw" to make copying easier*)
3. Create a file called `/_layouts/default.html` in your site
4. Paste the default layout content copied in the first step
5. Customize the layout as you'd like

### Customizing Google Analytics code

Google has released several iterations to their Google Analytics code over the years since this theme was first created. If you would like to take advantage of the latest code, paste it into `_includes/head-custom-google-analytics.html` in your Jekyll site.

## Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/BDHU/minimalist`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

## Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` once before the test script will work.

## Contributors

Special thanks to [@godalming123](https://github.com/godalming123) for adding dark mode support. Also thank [@solvaholic](https://github.com/solvaholic), [@tildehacker](https://github.com/tildehacker), and other contributors for making multiple bug fixes and improvements. All contributions are welcome.
