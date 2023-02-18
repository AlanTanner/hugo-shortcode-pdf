[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org) ![visitors](https://visitor-badge.glitch.me/badge?page_id=AlanTanner.pdfjs-hugo-module)
# pdfjs-hugo-module 
This is a fork of [hugo-embed-pdf-shortcode](https://github.com/anvithks/hugo-embed-pdf-shortcode) created by [Anvinth KS](https://github.com/anvithks) optimized for use as a Hugo Module. it uses the latest pre-built version of the PDF.js source code from [mozilla/pdfjs-dist](github.com/mozilla/pdfjs-dist).
---  
# Table of Contents  

* [Online Demo](https://polite-stone-0de443110.2.azurestaticapps.net/posts/pdfdemo/)
* [Introduction](#introduction)
* [Setup](#setup)  
* [Usage](#usage)  
* [FAQ](#faq)  
* [Support](#support)  
* [License](#license)  

---

## Introduction  
[\[Back to Top\]](#table-of-contents)

This is a [Hugo Shortcode](https://gohugo.io/extras/shortcodes/) developed for use in [Hugo](https://gohugo.io/) based websites. This shortcode allows you to embed a PDF file in a page on your Hugo website. It is developed using the [PDF.js](https://mozilla.github.io/pdf.js/) library by Mozilla.

![hugo-embed-pdf-shortcode cover](https://github.com/anvithks/hugo-embed-pdf-shortcode/blob/master/hugo-embed-pdf-cover.png)

## Setup  
[\[Back to Top\]](#table-of-contents)

**Note:**  This shortcode is for use in Hugo based websites. It will not work anywhere else. 

For beginners to Hugo Modules [click here](https://gohugo.io/hugo-modules/use-modules/) to read the offical documentation.

Init your project as a hugo module if not already.

```
hugo mod init <your_repo_url>
```

Add this module to site config. The following is an example of toml, and the same is true for yaml and json.

```
[[module.imports]]
    path = "github.com/AlanTanner/pdfjs-hugo-module"
```

<br />

## Usage  
[\[Back to Top\]](#table-of-contents)

In your Hugo website place the following shortcode in any of the markdown pages. 
```
{{< embed-pdf url="<path>/example.pdf" >}}

```

To hide pagination
```
{{< embed-pdf url="<path>/example.pdf" hidePaginator="true" >}}
```


To render a selected page number
```
{{< embed-pdf url="<path>/example.pdf" renderPageNum="5" >}}
```

To hide loading spinner
```
{{< embed-pdf url="<path>/example.pdf" hideLoader="true" >}}
```

### Parameters
- **url (required)** : The relative location of the file.  
- **hidePaginator (optional)**: Boolean which expects `true` or `false`. Hides the paginator for single page documents. 
- **renderPageNum (optional)**: Integer which expects any number from `1` up to the last page number in the document. Will render that specific page on initial load.
- **hideLoader (optional)**: Boolean which expects `true` or `false`. Hides the loading spinner while your document loads. 

<br />

**Note:** Currently supports local file embed. If absolute URL from the remote server is provided, configure the CORS header on that server.

## FAQ  
[\[Back to Top\]](#table-of-contents)

## Support  
[\[Back to Top\]](#table-of-contents)

You an reach me at:
- Twitter : [@alanctanner](https://twitter.com/alanctanner)

You can reach the orignal author of [hugo-embed-pdf-shortcode](https://github.com/anvithks/hugo-embed-pdf-shortcode) at:
- Twitter : [@anvith3](https://twitter.com/anvith3)

For any bugs, enhancement requests, feature requests please raise issues [here](https://github.com/AlanTanner/pdfjs-hugo-module/issues)

## License  
[\[Back to Top\]](#table-of-contents)

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
