# elearning-theme-fix

Fix [elearning.ua.pt](https://elearning.ua.pt) moodle page not being user friendly on mobile devices.  
This might happen because your account is linked to the default theme ```Adaptable```(Classic) and it should be using ```Boost``` instead.  
For more information on Moodle's Standard Themes [click here](https://docs.moodle.org/402/en/Standard_themes).

## Fix
Copy the following script to the Browser's Address Bar, **make sure ```javascript:``` is still there *(if not, write it manually)***, and press ENTER.
```javascript
javascript:window.location="https://elearning.ua.pt/theme/switchdevice.php?url=https://elearning.ua.pt/&device=mobile&sesskey="+M.cfg.sesskey
```

This script simply follows the given URL which changes the page theme. It passes the Moodle Session Key in the URL Parameter ```sesskey``` (mandatory).  
If you want to return to the Classic theme, change the URL Parameter ```device``` from '*mobile*' to '*default*'.  

If the browser does not allow you to run the script through the Address Bar, you can also run it inside the **Console** on ```DevTools``` *(F12 or CTRL + SHIFT + I)*, which is not straightforward if you are using Chrome on mobile [(how to here)](https://developer.chrome.com/blog/devtools-mobile/#easy-remote-debugging).

## Result

Moodle should go from the interface on the left, to the one on the right.
![elearning-themes](https://github.com/digas99/elearning-theme-fix/assets/45766898/c7be3520-34a0-4f5e-8eec-580618e20151)
