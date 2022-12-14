# Temporary MFA Code Generator

This is a tiny, simple TOTP authentication code generator.  It stores nothing, and
transmits nothing.  No cookies, no cloud, just HTML and JavaScript in the browser.

It works from a web server (of course), and also from local files.  Just have all the
files in the same folder and open `index.html`.

Copy the "secret key" for an "authenticator" app, paste it in, and it will start
generating codes.

## Why?

This can be used for testing, it can be an example for your application, or it might
solve a particular problem for you.

We had a requirement that temp employees NOT keep their cloud MFA keys on their
personal devices, but only in the company-provided password manager.  However, the
password manager required an email exchange to set up, and the email system required
MFA to get in.  With this, the cloud email system could be set up and logged into,
then the password manager could be set up, then the key copied from this tool into
the password manager.

## Credits

This is based on code from this very old post:
[www.thepolyglotdeveloper.com/2014/10/generate-time-based-one-time-passwords-javascript](https://www.thepolyglotdeveloper.com/2014/10/generate-time-based-one-time-passwords-javascript/),
modified for newer versions of the [jsSHA](https://github.com/Caligatio/jsSHA)
library.
