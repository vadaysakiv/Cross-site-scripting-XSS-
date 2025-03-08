**document.write(nameFromUrl);**
This directly writes the user input into the webpage.
If the input contains <script>alert(1)</script>, it gets executed immediately as part of the document.
document.write() is inherently unsafe because it processes scripts when writing to the document.

ReflectedXSS_V1

![image](https://github.com/user-attachments/assets/6fdc721d-8830-402d-8380-be85ce7e4d2d)



this version uses both **eval(nameFromUrl);**
and a dynamically created <script> tag to execute any JavaScript passed via the name parameter in the URL. Test it with:

yourpage.html?name=alert(1)

ReflectedXSS_V2

![image](https://github.com/user-attachments/assets/18ef28ba-6e62-4a7a-9265-41ab8046addf)



**eval(userInput); Executes Any JS
Example: ?input=alert(1) will execute immediately.**
