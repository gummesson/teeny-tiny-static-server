# README

*Teeny Tiny Static Server* is a small Rakefile for serving static files with [Rack](https://github.com/chneukirchen/rack "Rack"), [Rack-Rewrite](https://github.com/jtrupiano/rack-rewrite "Rack-Rewrite") and [Thin](https://github.com/macournoyer/thin "Thin").

## Usage

    rake server        Start the server
    rake open          Open the default port in a web browser
    rake launch        Open the default port in a web browser and start the server

## Configuration

The default folder used for the static files is `site`, the default port is `9292` and the log is set to `false`. This can easily be changed by editing the following at the top of the file:

     DIR = "site"
    PORT = 9292
     LOG = false

## Requirements

- [Rack](https://github.com/chneukirchen/rack "Rack")
- [Rack-Rewrite](https://github.com/jtrupiano/rack-rewrite "Rack-Rewrite")
- [Thin](https://github.com/macournoyer/thin "Thin")

## Why a Rakefile?

It's small and portable.

## License

**The MIT License (MIT)**

*Copyright (c) 2013 Ellen Gummesson*

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
