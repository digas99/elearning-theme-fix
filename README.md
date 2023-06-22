# elearning-theme-fix

## Issue
Fix [elearning.ua.pt](https://elearning.ua.pt) moodle page not being user friendly on mobile devices.  
This might happen because your account is linked to the theme ```Adaptable```(Classic) and it should be using ```Boost``` instead.  
[Click here](https://docs.moodle.org/402/en/Standard_themes) for more information on Moodle's Standard Themes.

## Fix
Copy the following script to the Browser's URL field, **make sure ```javascript:``` is still there *(if not, write it manually)***, and press ENTER.
```javascript
javascript:window.location="https://elearning.ua.pt/theme/switchdevice.php?url=https://elearning.ua.pt/&device=mobile&sesskey="+M.cfg.sesskey
```

This script simply follows the given URL which changes the page theme. It passes the Moodle Session Key in the URL Parameter ```sesskey``` (mandatory).  
If you want to return to the Classic theme, change the URL Parameter ```device``` from '*mobile*' to '*default*'.

## Result

Moodle should go from the interface on the left, to the one on the right.
![elearning-themes](https://github.com/digas99/elearning-theme-fix/assets/45766898/ae5ce28b-3f04-4bcc-abcb-2c014033b391)
