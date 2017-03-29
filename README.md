Register Country
================

The Register Country module is designed to intercept new registrations and check
if the IP address being used is registered to a country that the site
administrator has chosen. In this way, you may limit sign ups to your site to
specific countries.

Installation
------------
Normal module installation applies, however, there are some preparatory steps.

Before Enabling This Module
---------------------------

- You must install and enable the [IP-based determination of Country module](https://github.com/backdrop-contrib/ip2country) first.
Note: ip2country installs a VERY large database table (30+ MB); it will take a little while. Wait for it.
- Follow the instructions for the Error Page below.
- Now you can enable the Register Country module.

Settings
--------

- Enter the message you wish to show to visitors if they are denied 
registration.
- Enter the path for the error page. By default it is the Backdrop front page, 
or the site's 403 (Access denied) page if this has been set (this can be set at 
any time by visiting the page Configuration > System > Site information and 
filling in the 403 section).
- Decide what to do if a visitor's address is not matched by ip2country's 
IP address lookup. This is normally set to block, but it may be better for user
experience in territories where IP address lookup is unreliable (such as 
developing countries) to allow registration to proceed instead. If unmatched
registration is allowed, a message is logged in the site reports with the user's
IP address.
- Select as many countries as you need to which to limit your registration.
- Click the "Save configuration" button.

Yout site should now reject registration attempts from any countries not in 
your allowed list.

Creating a custom registration denied Page
------------------------------------------

- Use "Create content" to create a page.
- Set the title to something like "Registration Denied".
- Make sure comments are disabled and the page is "published" and not "promote to front page."


License
-------

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.

Current Maintainers
-------------------

- Docwilmot (https://github.com/docwilmot

Credits
-------

- Original developer: https://www.drupal.org/u/nancydru
