## XSS (Cross Site Requests)

* https://fin1te.net/articles/xss-on-facebook-via-png-content-types/
* https://news.ycombinator.com/item?id=11300395
  * 1. Don't serve user supplied content from a subdomain of your main site. Facebook fixed this by removing the redirect from photo.facebook.com to their CDN, so now user content comes from *.akamaihd.net.
  * 2. If a user uploads a PNG (or whatever), and you've validated it for that content type, don't serve it from your servers with a different content type. Clever users can make files that browsers will handle in different ways for different content types. Facebook's CDN still seems to allow serving files with the wrong (unvalidated) content type just by changing the file suffix in the URL.
