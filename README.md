js-intl
=======

Internationalisation i18n package for HTML5 & JavaScript, desgined to be used in Cordova applications.

The string databases are stored in the i18n subfolder in json format. The file name pattern is i18n/<language-code>.js.

All HTML tags can be translated by adding an data-i18n attribute. You can specify text inside of tags that get overridden by the application of i18n strings.

If strings need to be translated in JavaScript the function "_" can be used:

```javascript
var sometext = _('somekey');
```

In order to kick translation the function switchLanguage needs to be called. It can be called any time to switch to another language. Usually one will however just call switchLanguage once during 'documentready'.

```javascript
$(document).ready(function() {
	switchLanguage('de');
});
```

Or if used in conjunction with the Cordova globalisation plugin:

```javascript
navigator.globalization.getPreferredLanguage(function(language) {
	switchLanguage(language);
});
```

To view a demo that translates an English page to German [click here](https://rawgithub.com/steima/js-intl/master/demo.html).

This library depends on some modern jQuery version ;) tested with many ... they all worked!

It should be compatible if used with other JS frameworks. This library does NOT require jQuery to be bound to the $ sign.
