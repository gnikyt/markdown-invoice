# Markdown Invoice

This is a simple Symfony console application that I use to turn Markdown invoices into HTML or PDF.


## Setup

Simply create your invoice folders under `invoices/` directory. Example: paid, unpaid, estimates. A recommended file 
naming format is `[YYYY]-[MM]-[DD]-[project].md` (2013-01-15-github.md).

See `sample/` dirctory for an example invoice in Markdown and it's PDF output when generated.

## Useage

```bash
bin/markdown-invoice generate --help
Usage:
 generate [--output[="..."]] src [invoice]

Arguments:
 src                   Location of invoice; ex: "paid", "unpaid"
 invoice               What invoice to generate for?

Options:
 --output              Output to format; html or pdf (default: "html")
 --help (-h)           Display this help message.
 --quiet (-q)          Do not output any message.
 --verbose (-v)        Increase verbosity of messages.
 --version (-V)        Display this application version.
 --ansi                Force ANSI output.
 --no-ansi             Disable ANSI output.
 --no-interaction (-n) Do not ask any interactive question.
```

Example run:

```bash
bin/markdown-invoice generate unpaid --output=pdf
Please choose an invoice in "unpaid"...

1. 2012-01-15-xxxx.md
2. 2012-01-14-xxx.md
Which invoice? 2

Generating for invoice "2012-01-14-xxx"...

Invoice generated.
PDF saved to: output/2012-01-14-xxx.pdf
```

## Requirements

- [PHP](http://php.net) 5.4.x
- [wkhtmltopdf](http://code.google.com/p/wkhtmltopdf/)