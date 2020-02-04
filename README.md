# speedrun-OWASP-Juice-Shop
OWASP Juice-Shop in speedrun format

# Level 1
- Confidential Document
- DOM XSS
    - DOM based XSS is when the browser is dependant on user input to select an option or for navigation. For this issue to occure the user input must be referenced by a Java-Script script for the search and not sanitized there-fore allowing users to conduct code injection to the browser and allowing this to be sent to other users by simply sending them a URL.
    - (Answer) paste the DOM XSS code in the search bar and press enter.
- Error Handling
- Missing Encoding
- Outdated Whitelist
- Privacy Policy
- Reflected XSS
- Repetitive Registration
- Score Board
    - To get the scoreboard to appear in the OWASP juice box we must notice how each page is displayed through the URL and use that to find it
    - (Answer) at the end of the URL append /score-board to /#/
- Zero Stars
    - Using inspect element on the button which allows for the user to validate their feedback we see the difference between when all options which are required are filed is the 'disabled=true' Java-Script line, through this we can deduce that the user input is validated client side and that all we are required to change is this option and we should be able to bypass it.
    - (Answer) To solve this you have a choice between either editing the change 'disabled=true' to 'enabled=true' or just remove it all together to simulate the fields being complete.
