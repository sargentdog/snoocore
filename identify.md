---
title: snoocore identify with reddit
layout: default
---

# Identifying your app with Reddit

[Reddit has a set of API rules](https://github.com/reddit/reddit/wiki/API#wiki-rules) that outline how to identify your app using a `User-Agent` string. To set your `User-Agent`, make sure to include it when initializing Snoocore:

```javascript
var reddit = new Snoocore({ userAgent: 'myAppsName v0.0.5' });
/* every call after this uses the set userAgent */
```

## Browser?

If you are using snoocore in a browser based environment, you need to set `browser: true` to suppress errors such as:

> Refused to set unsafe header "User-Agent" 

The `User-Agent` will still be specified in requests as an additional parameter `app=<userAgent>` following a standard [RES](https://github.com/honestbleeps/Reddit-Enhancement-Suite) has laid out with their requests.