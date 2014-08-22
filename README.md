Aleph.js [![Build Status](https://travis-ci.org/sudodoki/Aleph.js.svg?branch=master)](https://travis-ci.org/sudodoki/Aleph.js)
========
>The Aleph's diameter was probably little more than an inch, but all space was there, actual and undiminished. Each thing (a mirror's face, let us say) was infinite things, since I distinctly saw it from every angle of the universe.
>
> -- <cite>[Jorge Luis Borges ][1]</cite>

## Reasoning behind this library
When working on client-side apps, which are either prototypes/POCs or are supposed to be thin clients, getting all the data from the server, the need for some random data to be used in code arise.
There's a great lib [Chance.js][2] and there's a great service [json-generator][3], which help greatly when in need of some random data for that matter, but you either need to know all the objects/properties you will need in advance, or you're going to use single object and call some methods on them.

**Aleph.js** can be considered a plain chance.js wrapper based on [ES6 Proxies][4], which gives you an opportunity to get random data by simply trying to access it in place, without need to call some methods or create new nested objects.

## How to use
### For node.js
1. Install library by running 

      npm install sudodoki/Aleph.js
2. Require it in your code 

      var Store = require('Aleph.js')
      var store = new Store()

### For browser
1. Install library by running

      bower install sudodoki/Aleph.js

2. Include bower_components/Aleph.js/bundled.js into your page.
You now have Aleph constructor globally available.

## Compatibility
This library is impelemented using [proxies][4], so it will run in environments, [that have support for it][5]. Generally speaking, it's Node behind `--harmony` flag and FF. This library also leverages [harmony-reflect][6] for getting some normalized goodies across different environments.
## API
## Todos

[1]:http://www.phinnweb.org/links/literature/borges/aleph.html
[2]:http://chancejs.com/
[3]:http://www.json-generator.com/
[4]:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy
[5]:http://kangax.github.io/compat-table/es6/#Proxy
[6]:https://github.com/tvcutsem/harmony-reflect