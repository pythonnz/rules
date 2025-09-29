# Constitution

This is Markdown source code to produce HTML (for https://python.nz) and PDF (for
printing).<br> _Note: On github.com, bullet points will show in addition to numbering
(styling is ignored). Also, empty HTML comments have been inserted to prevent wrong
indentation following unordered lists. The HTML/PDF results look fine._

#### Create HTML

Use [pandoc](https://pandoc.org):

```
pandoc -s constitution.md -o constitution.html -c constitution.css -V "pagetitle:Constitution"
```

(`-s` standalone = embed external CSS, `pagetitle` to suppress title warning without
inserting another headline)

#### Table of Contents

Optionally, `--toc` will also create a table of contents with headline links (handy but
not fit for PDF):

```
pandoc -s constitution.md -o constitution.html -c constitution.css -V "pagetitle:Constitution" --toc
```

#### Create PDF

Just print the HTML from your browser to a PDF file.<br> If you want to use a dedicated
conversion tool instead, check that it does the job correctly (the numbering of bullets
and sub bullets is where [weasyprint](https://weasyprint.org/) failed)
