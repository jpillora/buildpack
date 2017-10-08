## jpillora/buildpack

A simple buildpack with Go and Node installed

### Install

```
heroku config:set BUILDPACK_URL=http://github.com/jpillora/buildpack.git
```

Note

* Sets up a `GOPATH` so `go get <my-awesome-tool>` and `my-awesome-tool --help` will work

### Usage

1. Create a new app `foo`

1. Add a `run` file:

	``` sh
	#!/bin/sh

	npm i -g serve

	serve -p $PORT
	```

1. Commit and push

1. `foo`'s home is now being served

#### MIT License

Copyright © 2017 &lt;dev@jpillora.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.