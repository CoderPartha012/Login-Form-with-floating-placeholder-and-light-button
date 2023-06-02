# Login Form with Floating Placeholder

This is an HTML and CSS code for a user-friendly login form. The form consists of two input fields, one for the username and the other for the password.

## Features

- Gradient background color for the login box
- Box shadow and rounded corners for the login box
- Stylish input fields with changing color and movement on focus or content entry
- Hover effect on the login button with gradient background, text color change, and box shadow with multiple layers
- CSS animations on nested span elements within the anchor tag

## Usage

To use this login form, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/your-repository.git`
2. Open the HTML file in your preferred web browser.
3. Enter your username and password in the respective input fields.
4. Click the login button to submit the form.

## Example

```html
<div class="login-box">
  <input type="text" placeholder="Username" />
  <input type="password" placeholder="Password" />
  <a href="#" class="login-button">
    <span>Login</span>
  </a>
</div>
/* Example CSS code for the login form */
.login-box {
  background: linear-gradient(to bottom, #ffffff, #f2f2f2);
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 5px;
  padding: 20px;
}

.login-box input[type="text"],
.login-box input[type="password"] {
  border-bottom: 2px solid #ccc;
  transition: all 0.3s ease;
  width: 100%;
  padding: 10px 0;
  margin: 10px 0;
}

.login-box input[type="text"]:focus,
.login-box input[type="password"]:focus {
  border-bottom-color: #66afe9;
}

.login-button {
  display: inline-block;
  background: linear-gradient(to bottom, #3498db, #2980b9);
  color: #fff;
  text-align: center;
  padding: 10px 20px;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.login-button:hover {
  background: linear-gradient(to bottom, #3cb0fd, #3498db);
  color: #fff;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3), 0 3px 5px rgba(0, 0, 0, 0.2);
}

.login-button span {
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.login-button span:after {
  content: '\\00bb';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.login-button:hover span {
  padding-right: 25px;
}

.login-button:hover span:after {
  opacity: 1;
  right: 0;
}
