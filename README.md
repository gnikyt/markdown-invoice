# Markdown Invoice

This is a simple Symfony console application that I use to turn Markdown invoices into HTML or PDF.

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

## Requirements

- [PHP](http://php.net) 5.4.x