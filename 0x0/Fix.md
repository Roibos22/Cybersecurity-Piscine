In order to fix the vulnerability, all we need to do is comment out the three lines in the source code, that add the user input as a new script element. The new source code looks as follows:

<!DOCTYPE html>
<html>
<head>
    <title>Vulnerable XSS Example</title>
</head>
<body>
    <h1>XSS Vulnerability Example</h1>
    <p>This is a vulnerable page with an XSS vulnerability.</p>
    <form>
        <label for="inputText">Enter some text:</label>
        <input type="text" id="inputText">
        <button type="button" onclick="displayText()">Submit</button>
    </form>
    <div id="output"></div>
    <script>
        document.cookie = "ftCookies=If_You_See_Me_Its_Win";
        function displayText() {
            var userInput = document.getElementById("inputText").value;
            document.getElementById("output").innerHTML = "<b>" + userInput + "</b>";

            // var script = document.createElement("script");
            // script.textContent = userInput;
            // document.body.appendChild(script);
        }
    </script>
    <div id="cookieOutput"></div>
</body>
</html>


With theese changes we only show the userInput as text, but not append script elements anymore.