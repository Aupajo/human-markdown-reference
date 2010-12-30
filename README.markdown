# Human Markdown Reference

The Human Markdown Reference is a set of short, easy to understand HTML pages you can include in any project that uses Markdown.

**Important:** This is not designed to be a complete reference. Just a quick guide for the layman.

It's perfect for including as a pop-up help window next to your textarea.

See also: the Human Textile Reference.

## How To Use

[Download](http://github.com/Aupajo/human-markdown-reference/downloads) or clone this repository.

Copy the `markdown-reference/` directory to your project.

Add a help link to the reference:

### HTML Snippet


    You can format your text using
    <a href="markdown-reference/index.html"
       onclick="window.open(this.href,'markdown_reference','height=400,width=600,scrollbars=1'); return false;">Markdown</a>.
    </code>


### Rails Snippet

    You can format your text using
    <%= link_to 'Markdown', 'markdown-reference/index.html', :popup => ['markdown_reference', 'height=400,width=600,scrollbars=1'] %>


## Reference Sections

The reference sections include:

* Text formatting
* Links and images
* Headings
* Lists
* Special

## Notes

### Size

It's extremely lightweight; one HTML file, one minified CSS file, two images. If your web server has GZip compression switched on it should total 2.3KB.

### JavaScript

The guide uses JavaScript to toggle the different categories. If the browser's JavaScript is disabled, every category will be shown expanded, which is fine.

It uses jQuery 1.4.4 from the Google's AJAX CDN (the request should be a cache hit, so you'll incur no extra wait time).

### Sass

Included stylesheet is compiled using [Sass](http://sass-lang.com/). If you want to make modifications, alter `sass/markdown-reference.css`. You can output the compressed version with:

    sass sass/markdown-reference.scss markdown-reference/stylesheets/markdown-reference.css -t compressed

If you're developing, you can use Sass' `--watch` option.

