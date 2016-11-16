# FreeMember: Free your member templates!

FreeMember is a free add-on for ExpressionEngine 3.0+, which adds powerful inline member profile
& authentication tags using the native EE template syntax, instead of using the ugly and inflexible
static member templates bundled with EE.

## Requirements

* ExpressionEngine 3.0+
* PHP 5.3+

## Installation

1. Copy the `freemember` folder to `system/user/addons` on your server.
2. Create an encryption key in `config.php` if you have not already done so (see below).
3. Visit Developer > Add-On Manager on your server, and click Install next to FreeMember.

## How do I create an encryption key?

ExpressionEngine and CodeIgniter have a built in encryption class, which FreeMember uses to securely
store form parameters between page loads (such as required fields on your registration page).

Many ExpressionEngine add-ons use this library, so you may have already set an encryption key. If
you have not, you will see the following poorly worded error message when you try to use FreeMember
tags on your website:

> In order to use the encryption class requires that you set an encryption key in your config file.

Creating an encryption key is easy. Simply follow these steps:

1. Visit [this page](https://www.grc.com/passwords.htm) to generate a random key. **The key
   you generate must be unique for each ExpressionEngine site**. The *63 random alpha-numeric
   characters* box will do nicely. You could also use 1Password or similar to generate a random
   string - just be sure it is at least 32 characters long.
2. Open `system/expressionengine/config/config.php`. Scroll down to where you see
   `$config['encryption_key']`, and paste in your random string. For example:

```php
$config['encryption_key'] = "yourrandomstringhere";
```

That's it. Now your encryption key is set, and you're ready to start using FreeMember!

## Documentation

The following tags are available:

* [Login Tag](https://github.com/reusserdesign/freemember/blob/master/docs/login_tag.md)
* [Logout Url Tag](https://github.com/reusserdesign/freemember/blob/master/docs/logout_url_tag.md)
* [Register Tag](https://github.com/reusserdesign/freemember/blob/master/docs/register_tag.md)
* [Update Profile Tag](https://github.com/reusserdesign/freemember/blob/master/docs/update_profile_tag.md)
* [Members Tag](https://github.com/expressodev/reusserdesign/blob/master/docs/members_tag.md)
* [Forgot Password Tag](https://github.com/reusserdesign/freemember/blob/master/docs/forgot_password_tag.md)
* [Reset Password Tag](https://github.com/reusserdesign/freemember/blob/master/docs/reset_password_tag.md)

## Support

If you have found a bug, or would like to request a feature, please use the
[GitHub Issue Tracker](https://github.com/reusserdesign/freemember/issues?state=open).

If you have a question about using FreeMember, please check [ExpressionEngine Answers](http://expressionengine.stackexchange.com/)
to see whether anyone else has had the same issue, or ask a new question. Be sure to tag your question
with `freemember` so it can be easily found.

## Release Notes

For a complete list of changes in each FreeMember release, please see our [Changelog](https://github.com/reusserdesign/freemember/blob/master/CHANGELOG.md).

## License

FreeMember is released under the MIT License. For more information, see [License](https://github.com/reusserdesign/freemember/blob/master/LICENSE.md).
