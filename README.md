# cheerio

## Usage

1. Put 'cheerio.bundle.js' file in your cloud/ folder.
2. Require module in Cloud Code.

## Examples

```js
var cheerio = require('cloud/cheerio.bundle.js'),
    $ = cheerio.load('<h2 class="title">Hello world</h2>');

$('h2.title').text('Hello there!');
$('h2').addClass('welcome');

$.html();
//=> <h2 class="title welcome">Hello there!</h2>
```

```js
var cheerio = require('cloud/cheerio.bundle.js'),
    $ = cheerio.load('<p>paragraph 1</p> <p>paragraph 2</p> <p>paragraph 3</p>');

var list = $('p').map(function() {
  return $(this).text();
}).get();

//=> list = [ "paragraph 1", "paragraph 2", "paragraph 3" ]
```