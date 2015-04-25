A PHP Implementation of the Google AJAX Language API. It allows you to translate text between the languages supported by the Google Language API.

Please read the [Google Language API docs](http://code.google.com/apis/ajaxlanguage/documentation/) for more information.


## Example Usage ##

```
<?php
/**
* example usage
*/

// we need the page treated as utf-8, otherwise the encoding will be mangled
header('Content-Type: text/html; charset=utf-8');

// require google language api class
require_once('google.translator.php');

// translate text
$text = 'Welcome to my website.';
$trans_text = Google_Translate_API::translate($text, 'en', 'it');
if ($trans_text !== false) {
	echo $trans_text;
}
?>
```

The code is alpha, pre-release and may be buggy. To get the Alpha code, please [checkout the latest source from SVN](http://code.google.com/p/php-language-api/source/browse/trunk/google.translator.php).

### Attribution ###

Google [requires attribution for using their AJAX Language API](http://code.google.com/apis/ajaxlanguage/documentation/#Branding). However, using an API key is your choice.

### Disclamer ###

This project is not affiliated with Google. It is simply an implementation of their Language API in PHP.