# MailerQ EJS Plugin

## Installation

```bash
npm install mailer-q-ejs --save
```

## Usage

- This plugin is an extension of the [MailerQ](https://github.com/mailer-q/mailer-q) module for sending email.
- It enables MailerQ to use EJS templating to send email.
- To use this extension, simply require the module and call the resulting function with the path to your email templates as an argument.

Example configuration:

```javascript
const path = require("path");
const MailerQ = require("mailer-q")();
const MailerQEjs = require("mailer-q-ejs");

const options = {
  ...otherOptionsHere,
  renderer: MailerQEjs(path.join(__dirname, "./email_templates"))
};

module.exports = MailerQ.config(options);
```
