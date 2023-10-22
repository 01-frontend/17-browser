# Overview

https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work

## 1. Navigation

This is when the user `requests a page` by `entering a URL` into the address bar,` clicking a link`, `submitting a form`, as well as `other actions`

## 2. DNS Lookup

The first step of navigating to a web page is `finding where the assets` for `that page are located`. If you've `never visited this site`, a DNS lookup `must happen`

Your browser `requests a DNS lookup`, which is eventually fielded by a name server, which in `turn responds with an IP address`. After this initial request, `the IP` will likely be `cached for a time`

DNS lookups must be done for `each unique hostname` the requested page references. If your fonts, images, scripts, ads, and metrics all have different hostnames, a DNS lookup will have to be `made for each one`

## 3. TCP Handshake

Once the `IP address is known`, the browser `sets up a connection to the server` via `a TCP three-way handshake (SYN-SYN-ACK)` - because there are `three messages transmitted` by TCP to negotiate and `start a TCP session` between two computers

## 4. TLS Negotiation

`For secure connections` established over HTTPS, another "handshake" is required. This handshake, or rather the `TLS negotiation`, determines `which cipher will be used to encrypt` the communication, verifies the server, and establishes that a secure connection is in place `before beginning the actual transfer of data`

## 5. Response

Once we `have an established connection` to a web server. Once the server `receives the request`, it will `reply with relevant response headers` and `the contents of the HTML`

This response for this `initial request contains the first byte` of data received

`Time to First Byte (TTFB)` is the `time between` when the user `made the request` and the `receipt of this first packet of HTML`

## 6. Parsing

Parsing is the step `the browser takes to turn the data it receives` over the network `into the DOM and CSSOM`

## 7. Render

Rendering steps `include style, layout, paint` and, in some cases, `compositing`

The CSSOM and DOM trees created in the parsing step `are combined into a render tree` which is then `used to compute the layout` of every visible element, which is then painted to the screen

## 8. Interactivity

`Time to Interactive (TTI)` is the `measurement of how long it took` from that f`irst request which led to the DNS lookup and SSL connection` to `when the page is interactive`
