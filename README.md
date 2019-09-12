# A simple PHP CAPTCHA script

This packaged is modified version of [simple-php-captcha](https://github.com/yasirmturk/simple-php-captcha).

This code is the object oriented version of the original code.

I also tried to do minor improvements (dynamic path for fonts and background images)

_Licensed under the MIT license: http://opensource.org/licenses/MIT_

## Basic usage
0 - Install the package:
```
composer require alikhalili/simple-captcha
```

1- Create a captcha object:
```
$captcha = new Captcha();
```

2- Draw image
```
$captcha->config();
$image = $capthca->getImage();

//in the view
echo "<img src='$image' />";

//or in ajax response to a refresh request:
echo $image;
```
or validate the code:
```
$captchaIsValid = $captcha->verify($givenCode);
```

## Thanks
 - Thanks to Cory LaViska for the base code and Yasir M Türk for the [forked repository](https://github.com/yasirmturk/simple-php-captcha). 
 - Special thanks to Subtle Patterns for the patterns used for default backgrounds: http://subtlepatterns.com/
 - Special thanks to dafont.com for providing Times New Yorker: http://www.dafont.com/