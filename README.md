# Web Scraping using NodeJS

## using Basic HTTP Request

The first strategy makes an HTTP request to a URL and expects an HTML document string as the response. Retrieving the HTML is easy, but there are no browser APIs in NodeJS, so we need a tool like cheerio to process DOM elements and find the necessary metatags.

The advantage 👍 of this approach is that it is fast and simple, but the disadvantage 👎 is that it will not execute JavaScript and/or wait for dynamically rendered content on the client.

## Link Preview Function

An excellent use-case for this strategy is a link preview service that shows the name, description, and image of a 3rd party website when a URL posted into an app. For example, when you post a link into an app like Twitter, Facebook, or Slack, it renders out a nice looking preview.

Link previews are made possible by scraping the meta tags from <head> of an HTML page. The code requests a URL, then looks for Twitter and OpenGraph metatags in the response body. Several supporting libraries are used to make the code more reliable and simple.

#### cheerio is a NodeJS implementation of jQuery.

#### node-fetch is a NodeJS implementation of the browser Fetch API.

#### get-urls is a utility for extracting URLs from text.
