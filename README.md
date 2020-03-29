# Tales of my family
I set this site up to share stories from my family: some of them are about me, of course, but there are others here. It's not really a family tree kind of thing, although there will be information from various family genealogists and contributors.

The site is at [cullaloe.com/family/](https://cullaloe.com/family/). It is based upon the [Tufte-Jekyll theme](https://github.com/clayh53/tufte-jekyll) by photographer and coder [Clay Harmon](http://www.clayharmon.com/). I retain some of his notes in this README for quick reference, you should refer to his repository for further details for your own implementation.

## Configuration
This site uses custom plugins for things like latex math rendering, so the vanilla method of uploading and serving the content and stylesheets doesn't work on GitHub pages. The site is served from the /docs folder, which is configured as the source on GitHub. It is built offline, tested and uploaded to GitHub thus:

```sh
$ jekyll s -d docs
$ rake
```

## Custom Liquid tags
### Text

```
{% newthought "This will be rendered in small caps" %} blah blah

blah lorem blah{% sidenote "sidenote-id" "This is a random sidenote" %} blah blah

lorem nobeer toasty critters{% marginnote "margin-note-id" "Random thought when drinking" %} continue train of thought
```

### Images in the page body

Note that images need to be included *on their own line* in order for the captions to work correctly.

```
Full width, i.e. an image that spans both the main content column and the side column: 

{% fullwidth "assets/img/rhino.png" "A caption for the image" %}
```
```
Full width from remote URL:

{% fullwidth "http://example.com/image.jpg" "A caption for the image" %}
blah
```
```
Main content column image:

{% maincolumn "assets/img/rhino.png" "This is the caption" %}
```
```
{% maincolumn "http://example.com/image.jpg" "This is the caption" %}
```

### Margin figure

An image in the side column needs an id:

```
blah blah {% marginfigure "margin-figure-id" "assets/img/rhino.png" "This is the caption" %} blah
```
```
blah blah {% marginfigure "margin-figure-id" "http://example.com/image.jpg" "This is the caption" %} blah
```

### Mathjax

Wrap inline math in a tag pair: ```{% m %}mathjax expression{% em %}``` and wrap bigger block level stuff with ```{% math %}mathjax expression{% endmath %}```
