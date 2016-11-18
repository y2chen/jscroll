# jScroll - jQuery Plugin for Infinite Scrolling / Auto-Paging

[![Build Status](https://travis-ci.org/pklauzinski/jscroll.svg?branch=master)](https://travis-ci.org/pklauzinski/jscroll)
[![npm version](https://img.shields.io/npm/v/jscroll.svg)](https://www.npmjs.com/package/jscroll)
[![Bower version](https://img.shields.io/bower/v/jscroll.svg)](https://github.com/pklauzinski/jscroll)
[![Join the chat at https://gitter.im/pklauzinski/jscroll](https://badges.gitter.im/pklauzinski/jscroll.svg)](https://gitter.im/pklauzinski/jscroll?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Official site at [jscroll.com](http://jscroll.com/).

* Copyright &copy; 2011-2015, [Philip Klauzinski](http://gui.ninja)
* Current Version: 2.3.6
* Modifications by Yong Chen
* Dual licensed under the MIT and GPL Version 2 licenses.
* http://jscroll.com/#license
* http://www.opensource.org/licenses/mit-license.php
* http://www.gnu.org/licenses/gpl-2.0.html

Requires jQuery v1.4.3+

## Facebook Page

Follow us on Facebook for commit updates: http://www.facebook.com/jScroll.Infinite.Scrolling

## Usage

The `jscroll` method is called on the selector for which you want your scrollable content contained within. For example:

```javascript
$('.jscroll').jscroll();
```

The `jscroll` method takes an optional object literal as a parameter for overriding the default options. An example of how this can be done is shown below.

```javascript
$('.jscroll').jscroll({
    loadingHtml: '<img src="loading.gif" alt="Loading" /> Loading...',
    padding: 20,
    nextSelector: 'a.jscroll-next:last',
    contentSelector: 'li'
});
```

## Options

* `debug (false)` - When set to true, outputs useful information to the console display if the `console` object exists.
* `autoTrigger (true)` - When set to true, triggers the loading of the next set of content automatically when the user scrolls to the bottom of the containing element. When set to false, the required next link will trigger the loading of the next set of content when clicked.
* `autoTriggerUntil (false)` - Set to an integer great than 0 to turn off `autoTrigger` of paging after the specified number of pages. Requires `autoTrigger` to be `true`.
* `loadingHtml ('<small>Loading...</small>')` - The HTML to show at the bottom of the content while loading the next set.
* `loadingFunction` (false) - A JavaScript function to run after the loadingHtml has been drawn. Makes it possible to fire up a [jspin.js](https://github.com/fgnass/spin.js/) spinner or other effect
* `padding (0)` - The distance from the bottom of the scrollable content at which to trigger the loading of the next set of content. This only applies when autoTrigger is set to true.
* `nextSelector ('a:last')` - The selector to use for finding the link which contains the href pointing to the next set of content. If this selector is not found, or if it does not contain a href attribute, jScroll will self-destroy and unbind from the element upon which it was called.
* `contentSelector ('')` - A convenience selector for loading only part of the content in the response for the next set of content. This selector will be ignored if left blank and will apply the entire response to the DOM.
* `pagingSelector ('')` - Optionally define a selector for your paging controls so that they will be hidden, instead of just hiding the next page link.
* `dataType` - Optionally define if the fetched content is HTML (html), JSON (json), or some other format to be inserted via custom dataProcess function
* `dataURL` - Optionally define the path to a JSON file to be fetched
* `dataProcess ('')` - Optionally define a function to process the data returned by JSON call, or through some other custom method
* `callback (false)` - Optionally define a callback function to be called after a set of content has been loaded.

For more information on the `contentSelector` option and how it loads a response fragment, see the [jQuery documentation for the .load() method](http://api.jquery.com/load/).

## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt](http://gruntjs.com).


## LICENSES:

* MIT: http://www.opensource.org/licenses/mit-license.php
* GPL-2.0: http://www.gnu.org/licenses/gpl-2.0.html
