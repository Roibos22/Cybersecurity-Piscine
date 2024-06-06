The vulnerability is an XSS vulnerability:

After pressing the submit button, the function displayText gets triggered. This function does two things:
1. it changes the inner text of the Element 'output' to the userInput.
2. it appends a new script element to the body of thehtml file.

This is were the vulnerability lies. whatever we will enter in the input filed will be added to the html body as a script.
In order to display the document.cookie value we hence just have to enter:
    document.getElementById('cookieOutput').innerText=document.cookie;
This accesses the inner text value of the cookieOutput and sets it to the document.cookie value, what is exactly what was asked for in the subject.
