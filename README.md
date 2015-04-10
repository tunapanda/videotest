# videotest
A simple page with an HTML5-embedded video that plays on repeat and is loaded with a different name each time to prevent caching on the client side. In order for this to work, your sever will need to stip anything matching the regex `rand[0-9]+` from url filenames. For example, in nginx you would do this:

```
rewrite /PATH/TO/VIDEOTEST/rand[0-9]+(.*)$ /PATH/TO/VIDEOTEST/$1;
```
