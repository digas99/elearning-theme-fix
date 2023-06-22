# elearning-theme-fix
Fix Universidade de Aveiro's Moodle theme from *adaptable* to *boost* (mobile compatibility)

Copy the following script to the Browser's URL field, **make sure ```javascript:``` is still there** (if not, write it manually), and press ENTER.
```javascript
javascript:window.location="https://elearning.ua.pt/theme/switchdevice.php?url=https://elearning.ua.pt/&device=mobile&sesskey="+M.cfg.sesskey
```

This script simply follows the given URL which changes the page theme. It passes the Moodle Session Key as a URL Parameter (mandatory).

## Result
![elearning-themes](images/elearning-themes.png)
