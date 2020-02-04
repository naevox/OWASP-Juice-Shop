# speedrun-OWASP-Juice-Shop
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
