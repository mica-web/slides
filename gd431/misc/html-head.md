# Codepen

1. `<!doctype html>`
???
- tells the browser what to expect
- enforce standards mode and more consistent rendering in every browser possible
- HTML5
- If working with legacy code, may encounter other DOCTYPEs
--
1. `<html lang="en">`
???
- aids speech synthesis tools to determine what pronunciations to use
- lang tag helps translate the document
- even if your site is only in one language, users may want to translate the content
- BONUS:  lowercase elements and attributes; doublequotes
--

1. `<head></head>`
1. `<meta charset="UTF-8">`
???
- `charset` tells the browser what language and writing system you're using
- more than 107k characters found in 90 writing systems
- UTF isn't default in all browsers
- Should always be first after `head` so everything after it is parsed correctly
- Like the `doctype` getting this right means your content will be rendered correctly
- Example with and w/o proper character encoding: https://www.w3.org/International/questions/qa-what-is-encoding
--
1. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
1. `<meta http-equiv="X-UA-Compatible" content="ie=edge">`
???
- instruct IE to use the latest supported mode with edge mode
- not necessary if you're only supporting IE 11 and/or Edge
--
1. `<title>Document</title>`
???
- document’s title or name
- used in the browser (tab titles, bookmarks)
- SEO, Google results
- 
--
1. `<body></body>`

---
