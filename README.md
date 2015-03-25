# handlebars.numeral

    {{number n}}

Content helpers providing [Numeral](http://numeraljs.com) and [Wolsey](http://wolsey.solidgoldpig.com) functionality for [Handlebars](http://handlebarsjs.com)

### Version

0.1.0

### Installation

    npm install handlebars.numeral

### Registering the helpers

     var Handlebars = require("handlebars");
     var NumeralHelper = require("handlebars.numeral");
     NumeralHelper.registerHelpers(Handlebars);

### Using the helpers

#### number

Formats a number

*Assuming default en format 0,0[.]00*

    {{number 3000}}                   → «3,000»

    {{number 3000.2}}                 → «3,000.20»

    {{number 3000.234}}               → «3,000.23»

    {{number 3000.236}}               → «3,000.24»

    {{number 30000000}}               → «30,000,000»

Formats with an explicit format

    {{number "3000.2" "0"}}           → «3000»

    {{number "3000.2" "0.0"}}         → «3000.2»

    {{number "3000.234" "0,0[.]0"}}   → «3,000.2»

    {{number 30000000 "0a"}}          → «30m»

#### numeral

Outputs a number as words

    {{numeral 2001}}                  → «two thousand and one»

#### ordinal

Outputs a number as an ordinal

    {{ordinal 2001}}                  → «two thousand and first»

As a number

    {{ordinal true}}
    {{ordinal number=true}}           → «2001st»

#### currency

Formats a number as a currency

    {{currency 3000}}                 → «£3,000.00»
    {{currency 3000.236}}             → «£3,000.24»

#### byte

Outputs a number as an ordinal

    {{byte 2000000}}                  → «2MB»

### Tests

To run the tests, cd to the handlebars.numeral directory

    npm install && npm test### Unlicense

handlebars.numeral is free and unencumbered software released into 
the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>