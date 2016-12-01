
<!---

This README is automatically generated from the comments in these files:
ajax-cache.html  iron-request.html

Edit those files, and our readme bot will duplicate them over here!
Edit this file, and the bot will squash your changes :)

The bot does some handling of markdown. Please file a bug if it does the wrong
thing! https://github.com/PolymerLabs/tedium/issues

-->

##&lt;ajax-cache&gt;

The `ajax-cache` element exposes network request functionality.

```html
<ajax-cache
	cache
    auto
    url="https://www.googleapis.com/youtube/v3/search"
    params='{"part":"snippet", "q":"polymer", "key": "YOUTUBE_API_KEY", "type": "video"}'
    handle-as="json"
    on-response="handleResponse"
    debounce-duration="300"></ajax-cache>
```

This element is an overloaded replacement of `iron-ajax` it includes the `cache` property which enabled 
storing requests as <k,v> pairs in PouchDb.

With `auto` set to `true`, the element performs a request whenever
its `url`, `params` or `body` properties are changed. Automatically generated
requests will be debounced in the case that multiple attributes are changed
sequentially.

Note: The `params` attribute must be double quoted JSON.

You can trigger a request explicitly by calling `generateRequest` on the
element.



##&lt;iron-request&gt;

iron-request can be used to perform XMLHttpRequests.

```html
<iron-request id="xhr"></iron-request>
...
this.$.xhr.send({url: url, body: params});
```


