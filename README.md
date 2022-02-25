# MkDocs Embed External Markdown Plugin

[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/fire1ce/3os.org/tree/master/src)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://mit-license.org/)

## About

MkDocs Embed External Markdown plugin that allow to inject **section** or all **full markdown** content from a given url.
The goal is to show different markdown from different sources inside your MkDocs project.

## Installation

Install the package with pip:

```bash
pip install mkdocs-embed-external-markdown
```

## Configuration

Enable the plugin in your `mkdocs.yml` file:

```yaml
plugins:
  - external-markdown
```

## Usage

- Section defined by **"##"** header (h2)
- **"#"** header (h1) will be **removed** from sorce content so you can use use your own header
- **"##"** header (h2) will be **removed** from sorce **section** content so you can use use your own header
- Supports multiple **sections** from any source

external_markdown requiress 2 parameters: **url** and **section name**.

```makrdown
{{ external_markdown('url', 'section name') }}
```

### Full markdown content

Embed full markdown content from a given url, you can use the following example:

```markdown
{{ external_markdown('https://raw.githubusercontent.com/fire1ce/DDNS-Cloudflare-Bash/main/README.md', '') }}
```

### Specific section

Embed markdown section from a given url, you can use the following example:

```markdown
{{ external_markdown('https://raw.githubusercontent.com/fire1ce/DDNS-Cloudflare-Bash/main/README.md', 'Installation') }}
```

## MkDocs Example

The following example shows how to use the plugin in mkdocs project:

```markdown
# Example Page

This is an example page.

## Embeding multiple markdown sections from different urls

### First Embedded Section

{{ external_markdown('https://raw.githubusercontent.com/mkdocs/mkdocs/master/README.md', 'Features') }}

### Second Embedded Section

{{ external_markdown('https://raw.githubusercontent.com/squidfunk/mkdocs-material/master/README.md', 'Quick start') }}
```

Will produce the following page:

![MkDocs Embed External Markdown Plugin](https://user-images.githubusercontent.com/16795594/155761254-17b47e65-d27e-438b-a476-15bd04fdc3ec.jpg)

## License

### MIT License

Copyright© 3os.org @2020

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to
deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or
sell copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
IN THE SOFTWARE.
