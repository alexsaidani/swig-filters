Swig Filters
=======

A collection of Swig template filters.


## Installing

To install the latest release version:

```bash
npm install --save swig-filters
```

To install the latest development version:

```bash
npm install git+https://github.com/belsrc/swig-filters.git#develop
```


In your application's server.js file simply require swig-filters, passing
the Swig object.

```javascript
var swig = require('swig');

require('swig-filters')(swig);
```

## Available Filters

#### currency(input[, sign])
```handlebars
{# foo = 102432.56 #}

{{ foo | currency('$') }}

{# => $102,432.56 #}
```

#### humanable(input)
```handlebars
{# foo = 'this-is-a-slug'; #}

{{ foo | humanable }}

{# => This is a slug #}
```

#### past_tense(input)
```handlebars
{# foo = 'code' #}

{{ foo | past_tense }}

{# => coded #}


{# foo = 'panic' #}

{{ foo | past_tense }}

{# => panicked #}


{# foo = 'laugh' #}

{{ foo | past_tense }}

{# => laughed #}
```

#### percent(input[, decimals])
```handlebars
{# foo = 0.98645 #}

{{ foo | percent(2) }}

{# => 98.64% #}


{# foo = 0.98645 #}

{{ foo | percent }}

{# => 98% #}
```

#### round(input[, decimals])
```handlebars
{# foo = 102432.563453 #}

{{ foo | round(2) }}

{# => 102432.56 #}
```

#### trim(input)
```handlebars
{# foo = '  This is some text. \n'; #}

{{ foo | trim }}

{# => This is some text. #}
```

#### truncate(input[, length[, end]])
```handlebars
{# foo = 'This is some text.'; #}

{{ foo | truncate(5) }}

{# => This ... #}
```


## License

Swig Filters is copyright (c) 2015 Bryan Kizer and licensed under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
