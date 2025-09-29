# Code of Conduct

This is Markdown source code to produce HTML (for https://python.nz) and PDF (for
printing).

#### Create HTML

Use [pandoc](https://pandoc.org):

```
pandoc -s code-of-conduct.md -o code-of-conduct.html -V "pagetitle:Code of Conduct"
```

(`-s` standalone, `pagetitle` to suppress title warning without inserting another
headline)

#### Create PDF

Just print the HTML from your browser to a PDF file.<br> If you want to use a dedicated
conversion tool instead, we've successfully used [weasyprint](https://weasyprint.org/):

```
weasyprint code-of-conduct.html code-of-conduct.pdf
```
