#jQuery component

jQuery with [component](https://github.com/component/component) support

Automatically synchronized with basic `jquery/jquery` repository with [componentor](http://github.com/edjafarov/componentor)

#### jquery decomposed
Instead of using custom builds the jQuery was decomposed on separate components per existing configuration:
```javascript
{ flag: "wrap", src: "src/wrap.js" },
{ flag: "css", src: "src/css.js" },
{ flag: "event-alias", src: "src/event-alias.js" },
{ flag: "ajax", src: "src/ajax.js" },
{ flag: "ajax/script", src: "src/ajax/script.js", needs: ["ajax"]  },
{ flag: "ajax/jsonp", src: "src/ajax/jsonp.js", needs: [ "ajax", "ajax/script" ]  },
{ flag: "ajax/xhr", src: "src/ajax/xhr.js", needs: ["ajax"]  },
{ flag: "effects", src: "src/effects.js", needs: ["css"] },
{ flag: "offset", src: "src/offset.js", needs: ["css"] },
{ flag: "dimensions", src: "src/dimensions.js", needs: ["css"] },
{ flag: "deprecated", src: "src/deprecated.js" },

```
* jquerycomp/jquery - complete jquery framework build
* jquerycomp/jquery-core - core jquery with sizzler
* jquerycomp/wrap
* jquerycomp/css
* jquerycomp/event-alias
* jquerycomp/ajax
* jquerycomp/ajax-script
* jquerycomp/ajax-jsonp
* jquerycomp/ajax-xhr
* jquerycomp/effects
* jquerycomp/offset
* jquerycomp/dimensions
* jquerycomp/deprecated

dependencies for separate components will be resolved automatically by component  framework.

#### usage

I assume you use [component](https://github.com/component/component) or [compy](https://github.com/edjafarov/compy)

```
$ component install jquerycomp/jquery
//or
$ compy install jquerycomp/jquery
```
in the code
```
var $ = require('jquery');
```

##### made by [@edjafarov](https://twitter.com/edjafarov)
