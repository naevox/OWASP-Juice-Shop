# OWASP-Juice-Shop
OWASP Juice-Shop in speedrun format

# Level 1
- Confidential Document
    - Confidential documents are generally stored on the same machine which the user has chosen to use. This document category can be defined by documents which the user does not wish for others to have access to.
    - (Answer) A solution based on arbritary experience changing the '/#/' to '/ftp/' you are able to navigate to an FTP server being hosted on the same server as the web-page herefore allowing users to access confidential documents.
- DOM XSS
    - DOM based XSS is when the browser is dependant on user input to select an option or for navigation. For this issue to occure the user input must be referenced by a Java-Script script for the search and not sanitized there-fore allowing users to conduct code injection to the browser and allowing this to be sent to other users by simply sending them a URL.
    - (Answer) paste the DOM XSS code in the search bar and press enter.
- Error Handling
    - When a program encounters an error it either fails gracefully in a way which the developer has defined or it crashes leaving any continuation to deadlock in a not so graceful fashion. At times this can be a large error such as causing the program or system to crash as whole.
    - (Answer) to cause an ungraceful error to occure we simply go into the '/ftp/' directory which we found and open any file which is not .md or .pdf, such as the .url files in the quarantine sub-directory.
- Missing Encoding
    - For the image to display the name has to given to the server in a href fashion. Unfortunately for this website the developer didn't program to protect against accidental issues with special characters being interpreted by the browser instead of being protected agaisnt accidental execution. The issue seen here is the developer has directly referenced file name in the HTML href without encoding leaving the # in the file name to be executed as a comment in the HTML form.
    - (Answer) change the href for the image from '#' to '%23' which is a URL encoded version of # which will be interpreted by the server but ignored by the browser.
- Outdated Whitelist
    - When options and features are removed from browser code they can be simply either commented out or the feature removed but the back-end is left. This can cause issues such as browser load time as the commented out code is still compiled but ignored, leave holes in the security which can add to the file size or offer individuals the option to still use un-supported services.
    - (Answer) go on devtools and go to the debugger option. From here navigate the different Java-Script classes and look for the keyword 'redirect' and add the redirect to the application URL.
- Privacy Policy
    - When scoping a penetration test we have to test each and every page which users have access to, this includes the policy page which shows the policy of the website and/ or company.
    - (Answer) navigate to 'https://bobbox.herokuapp.com/#/privacy-security/privacy-policy'
- Reflected XSS
    - Reflective XSS is Java-Script data which is saved temporarily on the browser but is removed once the user refreshes the page. This can be injected code which is temporarily available and referenced from the URL but will generally disapear if the user instead navigates or refreshes the page by clicking the href hyperlink to the current page.
    - (Answer) Not complete as Juice-Shop is being hosted using heroku.
- Repetitive Registration (DRY principle)
    - The dry principle states that all user logic should solely occure only once. When registering a new user into the application we can check for this validation through the password validation. Entering a password of 5 characters or more in the first input we get an acceptance message, repeating this on the second password field we also get an acceptance message. Changing the first input after the second is accepted gives an acceptance massage, this means that the password fields are fully independant with repeated logic causing an error allowing for unautheristed passwords.
    - (Answer) when creating a new user place password of 5 characters and repeat on second field, change first field input after second field is validated and proceed with user creation.
- Score Board
    - To get the scoreboard to appear in the OWASP juice box we must notice how each page is displayed through the URL and use that to find it
    - (Answer) at the end of the URL append /score-board to /#/
- Zero Stars
    - Using inspect element on the button which allows for the user to validate their feedback we see the difference between when all options which are required are filed is the 'disabled=true' Java-Script line, through this we can deduce that the user input is validated client side and that all we are required to change is this option and we should be able to bypass it.
    - (Answer) To solve this you have a choice between either editing the change 'disabled=true' to 'enabled=true' or just remove it all together to simulate the fields being complete.


# Level 2
- Admin Section
- Classic Stored XSS
- Deprecated Interface
- Fire-Star Feedback
- Login Admin
- Login MC SafeSearch
- Password Strength
- Security Policy
- View Basket
- Weird Crypto
