# puppetter-lazyload

Verifies that components/images on the page which are lazy loaded do not use scroll

# Usage:

- Install dependencies
  Run `npm i`

- to get help run `node lazyload.js -h`

- Example run `node lazyload.js --url=https://dev.apartmentlist.me/ca/san-francisco  -m
`

* Usage Examples:
*
*     node lazyload.js -h
*     // PASSES. Uses IntersectionObserver and lazyimages.js checks image visibility on page load without needing scroll events.
*     node lazyload.js --url=https://rawgit.com/GoogleChromeLabs/puppeteer-examples/master/html/lazyload.html
*     // FAILS. uses scroll events.
*     node lazyload.js --url=https://css-tricks.com/examples/LazyLoading/
*     // FAIL. Uses scroll events.
*     node lazyload.js --url=http://dinbror.dk/blazy/ -o results.html --save
*
