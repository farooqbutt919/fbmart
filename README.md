# fbmart
FB-Mart HTML Documentation
Overview
The FB-Mart HTML page is designed for a grocery service named "FB-Mart." It consists of a user interface with a heading, subheading, and forms for API calls and email subscriptions. The page is styled for a pleasant user experience.

Contents
Styles
Script Imports
API Call Function
Load Script Function
AWS SDK Configuration
Subscribe Function
HTML Structure
Styles
The styles section defines the visual appearance of the HTML elements. It includes the background color, font styles, and button styles.

css
Copy code
body {
    background-color: #090e14;
    color: #FF9900;
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

#heading {
    font-size: 36px;
    color: #eb770b;
    margin: 20px 0;
}

#subheading {
    font-size: 18px;
    margin-bottom: 20px;
    color: #eb770b;
}

form {
    display: flex;
    flex-direction: column;
    max-width: 300px;
    margin: 0 auto;
}

label {
    margin-bottom: 10px;
}

input {
    padding: 8px;
    margin-bottom: 15px;
    font-size: 16px;
}

button {
    background-color: #eb770b;
    color: #090e14;
    padding: 10px;
    font-size: 18px;
    cursor: pointer;
    border: none;
    margin-bottom: 15px; /* Added spacing after the button */
}

button:hover {
    background-color: #FF9900;
}
Script Imports
The script imports section includes the AWS SDK script and custom JavaScript code for API calls and email subscriptions.

html
Copy code
<script src="https://cdnjs.cloudflare.com/ajax/libs/aws-sdk/2.1051.0/aws-sdk.min.js"></script>
<script>
    // ... (JavaScript code)
</script>
API Call Function
The callAPI function is responsible for making an API call using the fetch function. It sends a POST request to the specified API endpoint with the provided first name and last name.

javascript
Copy code
var callAPI = (firstName, lastName) => {
    // ... (API call code)
}
Example usage:

html
Copy code
<button type="button" onclick="callAPI('John', 'Doe')">What's In the Grocery</button>
Load Script Function
The loadScript function dynamically loads scripts and executes a callback once the script is loaded.

javascript
Copy code
function loadScript(url, callback) {
    // ... (Script loading code)
}
Example usage:

javascript
Copy code
loadScript("https://example.com/script.js", function() {
    // Callback code
});
AWS SDK Configuration
The AWS SDK is configured with the provided access key, secret key, and region.

javascript
Copy code
AWS.config.update({
    accessKeyId: '', // Update with your AWS access key
    secretAccessKey: '', // Update with your AWS secret key
    region: 'us-east-1', // Update with your AWS region
});
Subscribe Function
The subscribe function initiates SES email verification for the provided email address.

javascript
Copy code
var subscribe = async (email) => {
    // ... (SES verification code)
}
Example usage:

html
Copy code
<button type="button" onclick="subscribe('example@email.com')">Subscribe</button>
HTML Structure
The HTML structure includes the heading, subheading, and forms for API calls and email subscriptions.

html
Copy code
<h1 id="heading">FB-Mart</h1>
<p id="subheading">Executive service to address your cravings during office hours</p>
<form>
    <!-- ... (Form elements) -->
</form>
This documentation provides a detailed explanation of the FB-Mart HTML code, including styles, scripts, and functionality. Feel free to customize it further based on your specific requirements.
