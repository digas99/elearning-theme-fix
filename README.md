# elearning-theme-fix

Fix [elearning.ua.pt](https://elearning.ua.pt) moodle page not being user friendly on mobile devices.  
This might happen because your account is linked to the default theme ```Adaptable```(Classic) and it should be using ```Boost``` instead.  
For more information on Moodle's Standard Themes [click here](https://docs.moodle.org/402/en/Standard_themes).

## Fix

1. Navigate to any [elearning.ua.pt](https://elearning.ua.pt) page (make sure you're logged in)
2. Copy the following script to the Address Bar - **make sure ```javascript:``` is still there when you paste it *(if not, write it manually)***
```javascript
javascript:window.location="https://elearning.ua.pt/theme/switchdevice.php?url=https://elearning.ua.pt/&device=mobile&sesskey="+M.cfg.sesskey
```
3. Press ENTER (or any similar action) to run the script

This script simply follows the given URL which changes the page theme. It passes the Moodle Session Key in the URL Parameter ```sesskey``` (mandatory), which is the reason why it must be a script (and not a plain URL).  
If you want to return to the Classic theme, change the URL Parameter ```device``` from '*mobile*' to '*default*'.  

To understand what the script does [click here](https://developer.mozilla.org/en-US/docs/Web/API/Window/location#example_1_navigate_to_a_new_page).

If the browser does not allow you to run the script through the Address Bar, you can also run it inside the **Console** on ```DevTools``` *(F12 or CTRL + SHIFT + I)*, which is not straightforward if you are using Chrome on mobile [(how to here)](https://developer.chrome.com/blog/devtools-mobile/#easy-remote-debugging).  

If still in doubt, this is how the script should look like in the Address Bar:
![elearning-themes-script](https://github.com/digas99/elearning-theme-fix/assets/45766898/7e60ed48-20cb-4ae5-820d-bf2cb5d4b5d9)

> **Note**
> *It is not clear if running the above script on one device will change the theme for all devices (it might, I'm not sure) so you should run it on whatever device you want the theme to change.*

## Result

Moodle should go from the interface on the left, to the one on the right.
![elearning-themes](https://github.com/digas99/elearning-theme-fix/assets/45766898/c7be3520-34a0-4f5e-8eec-580618e20151)
