Note: This branch and README covers the upcoming 2.0 release. View [1.x docs here](https://github.com/quilljs/quill/tree/1.3.6).

<h1 align="center">
  <a href="https://quilljs.com/" title="Quill">Quill Rich Text Editor</a>
</h1>
<p align="center">
  <a href="https://quilljs.com/" title="Quill"><img alt="Quill Logo" src="https://quilljs.com/assets/images/logo.svg" width="180"></a>
</p>
<p align="center">
  <a title="Quickstart" href="#quickstart"><strong>Quickstart</strong></a>
  &#x2022;
  <a title="Documentation" href="https://quilljs.com/docs/"><strong>Documentation</strong></a>
  &#x2022;
  <a title="Development" href="https://github.com/quilljs/quill/blob/master/.github/DEVELOPMENT.md"><strong>Development</strong></a>
  &#x2022;
  <a title="Contributing" href="https://github.com/quilljs/quill/blob/master/.github/CONTRIBUTING.md"><strong>Contributing</strong></a>
  &#x2022;
  <a title="Interactive Playground" href="https://quilljs.com/playground/"><strong>Interactive Playground</strong></a>
</p>
<p align="center">
  <a href="https://travis-ci.org/quilljs/quill" title="Build Status">
    <img src="https://travis-ci.org/quilljs/quill.svg?branch=master" alt="Build Status">
  </a>
  <a href="https://npmjs.com/package/quill" title="Version">
    <img src="https://img.shields.io/npm/v/quill.svg" alt="Version">
  </a>
  <a href="https://npmjs.com/package/quill" title="Downloads">
    <img src="https://img.shields.io/npm/dm/quill.svg" alt="Downloads">
  </a>
</p>
<p align="center">
  <a href="https://saucelabs.com/u/quill" title="Test Status">
    <img src="https://cdn.quilljs.com/badge.svg?v=2" alt="Test Status">
  </a>
</p>

[Quill](https://quilljs.com/) is a modern rich text editor built for compatibility and extensibility. It was created by [Jason Chen](https://twitter.com/jhchen) and [Byron Milligan](https://twitter.com/byronmilligan) and actively maintained by [Slab](https://slab.com).

To get started, check out [https://quilljs.com/](https://quilljs.com/) for documentation, guides, and live demos!


## Quickstart

Instantiate a new Quill object with a css selector for the div that should become the editor.

```html
<!-- Include Quill stylesheet -->
<link href="https://cdn.quilljs.com/1.0.0/quill.snow.css" rel="stylesheet">

<!-- Create the toolbar container -->
<div id="toolbar">
  <button class="ql-bold">Bold</button>
  <button class="ql-italic">Italic</button>
</div>

<!-- Create the editor container -->
<div id="editor">
  <p>Hello World!</p>
</div>

<!-- Include the Quill library -->
<script src="https://cdn.quilljs.com/1.0.0/quill.js"></script>

<!-- Initialize Quill editor -->
<script>
  var editor = new Quill('#editor', {
    modules: { toolbar: '#toolbar' },
    theme: 'snow'
  });
</script>
```

Take a look at the [Quill](https://quilljs.com/) website for more documentation, guides and [live playground](https://quilljs.com/playground/)!


## Download

- [npm](https://www.npmjs.com/package/quill) - `npm install quill`
- tar - https://github.com/quilljs/quill/releases


### CDN

```html
<!-- Main Quill library -->
<script src="//cdn.quilljs.com/1.0.0/quill.js"></script>
<script src="//cdn.quilljs.com/1.0.0/quill.min.js"></script>

<!-- Theme included stylesheets -->
<link href="//cdn.quilljs.com/1.0.0/quill.snow.css" rel="stylesheet">
<link href="//cdn.quilljs.com/1.0.0/quill.bubble.css" rel="stylesheet">

<!-- Core build with no theme, formatting, non-essential modules -->
<link href="//cdn.quilljs.com/1.0.0/quill.core.css" rel="stylesheet">
<script src="//cdn.quilljs.com/1.0.0/quill.core.js"></script>
  ```


## Community

Get help or stay up to date.

- [Contribute](https://github.com/quilljs/quill/blob/develop/.github/CONTRIBUTING.md) on [Issues](https://github.com/quilljs/quill/issues)
- Follow [@jhchen](https://twitter.com/jhchen) and [@quilljs](https://twitter.com/quilljs) on Twitter
- Ask questions on [Stack Overflow](https://stackoverflow.com/questions/tagged/quill)
- If privacy is required, email support@quilljs.com


## License

BSD 3-clause





Instruction to install old ruby on Windows is next.
Saved for myself some of them are from comments on github.

First of all remove dist folder. Removing can be done anytime.

Download ruby 2.1.4


Then we need to update openSSL

Thanks for the guy here https://github.com/oneclick/rubyinstaller2/issues/53#issuecomment-311356528. Go give him like saved me alot of time.

those below were copypasted from above comment
ridk enable
pacman -S mingw-w64-x86_64-openssl
gem install openssl
cp c:/msys64/mingw64/bin/libeay32.dll c:/msys64/mingw64/bin/ssleay32.dll c:/Ruby24-x64/bin/ruby_builtin_dlls/
ruby -ropenssl -e "puts OpenSSL::OPENSSL_LIBRARY_VERSION"

then we need to execute comands one by one.
all bellow are copypasted from packange.json. its just on windows they aren`t working because of linux command rm. Anyway thanks for authors of quill.

npm install
bundler install

npm run lint
webpack --config _develop/webpack.config.js


And thats all easy as eating a pie.
you better remove dist folder before doing it.

dist folder should be generated if everything is ok.
