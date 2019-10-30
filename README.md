---
order: 1
---
# Getting started

The NVDB API is a REST api with extensive search- and filter capabilities, as well as options for fine tuning which 
data elements to include in the respons. 

## Formats

The response formats from the API may be either XML or JSON (default), which you chooose using the 
standard http `accept` header. The format is versioned, and to ensure your application 
does not break upon format improvements we highly recomend you explsit control the version number, using this syntax: 
```
Accept: application/vnd.vegvesen.nvdb-v3-rev1+json
Accept: application/vnd.vegvesen.nvdb-v3-rev1+xml
```

The standard media types `application/json`and `application/xml` will always return the newest format version.


## Tracking requests and sessions

At least one of these http headers must be set by the client: 
```
"X-Client" :  "your@email", or other identification
"User-Agent" : "Name of your fantastic system" 
```
We really, really appreciate if at least one of these, preferably both, are given meaningful names. It gives us valuable 
information about who uses our API, and for what purpose. In addition, we also recommend (and appreciate) that you track your session using the `X-Client-Session` set to UUID or something similar. 

The API response will contain the header `X-REQUEST-ID`, which is probably useful if you need to report a problem. 

## Pagination 

