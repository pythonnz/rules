# Python New Zealand - Rules

Official rules of [Python New Zealand](https://python.nz).<br>
This repository holds the authoritative source code of the documents and tracks changes to them.

* Constitution
* Bylaws
* Code of Conduct

## How to create documents

### Constitution

This is Markdown source code to produce HTML (for https://python.nz) and PDF (for printing)<br>
*Note: On github.com, bullet points will show in addition to numbering (styling is ignored)*

#### Create HTML

Use [pandoc](https://pandoc.org):
```
pandoc -s constitution.md -o constitution.html -c constitution.css -V "pagetitle:Constitution"
```
(`-s` standalone = embed external CSS, `pagetitle` to suppress title warning without inserting another headline)

#### Table of Contents

Optionally, `--toc` will also create a table of contents with headline links (handy but not fit for PDF)
```
pandoc -s constitution.md -o constitution.html -c constitution.css -V "pagetitle:Constitution" --toc
```

#### Create PDF

Use [weasyprint](https://weasyprint.org) or similar, or just print from  your browser:
```
weasyprint constitution.html constitution.pdf
```

