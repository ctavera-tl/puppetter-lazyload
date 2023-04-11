# puppetter-lazyload

Verifies that components/images on the page which are lazy loaded do not use scroll

# Usage:

- Install dependencies Run `npm i`

- To get help run `node lazyload.js -h`

- Example run `node lazyload.js --url=https://dev.apartmentlist.me/ca/san-francisco  -m
`

# Options:

| Option                     | Description                                                | default value                      |     |     |
| -------------------------- | ---------------------------------------------------------- | ---------------------------------- | --- | --- |
| --version                  | Show version number                                        | [boolean]                          |     |     |
| -m, --useMobile            | Use mobile viewport                                        | [default: false]                   |     |     |
| -b, --useBot               | Use Bot crawler user agent                                 | [default: false]                   |     |     |
| -s, --save                 | Save screenshots to disk                                   | [default: false]                   |     |     |
| -u, --url                  | URL to load                                                | [string] [required]                |     |     |
| -o, --output               | Output HTML file                                           | [string] [default: "results.html"] |     |     |
| --scroll                   | Filename for screenshot of scrolled page. Only worked with |                                    |     |     |
| --save option.             | [default: "page_scroll.png"]                               |                                    |     |     |
| --noscroll                 | Filename for screenshot of non-scrolled page. Only worked  |                                    |     |     |
| with --save option.        | [default: "page_noscroll.png"]                             |                                    |     |     |
| --diff                     | Filename for diff screenshot between pages.                |                                    |     |     |
| [default: "page_diff.png"] |                                                            |                                    |     |     |
| --help                     | Show help                                                  | [boolean]                          |     |     |

- Usage Examples:
-
-     node lazyload.js -h
-     // PASSES. Uses IntersectionObserver and lazyimages.js checks image visibility on page load without needing scroll events.
-     node lazyload.js --url=https://rawgit.com/GoogleChromeLabs/puppeteer-examples/master/html/lazyload.html
-     // FAILS. uses scroll events.
-     node lazyload.js --url=https://css-tricks.com/examples/LazyLoading/
-     // FAIL. Uses scroll events.
-     node lazyload.js --url=http://dinbror.dk/blazy/ -o results.html --save
-
