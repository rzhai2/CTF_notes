## Intro To Burp
There are somethings that need to be remembered:
1. To config Burpsuite to listen on a specific browser, config the browser's proxy to be burp's ip and port.
2. Config Burpsuite to be consistent with the ip and port specified on the browser.
3. Update the Burpsuite certificate and import it on the browser.
4. Key point is that there seems to be no parameter checks on the server side, so there is no checking on whether it is a number, whether it is a text, or whether there is an OTP field. Removing the OTP field completely will bypass the check.
5. OTP is one time password. Essentially, it's a "something you have" factor in multi-factor authentication.