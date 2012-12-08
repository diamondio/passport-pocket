# Passport-Pocket 

[Passport](http://passportjs.org/) strategy for authenticating with [Pocket](http://getpocket.com)
using the OAuth 1.0a API.

This module lets you authenticate using Pocket in your Node.js applications.
By plugging into Passport, Twitter authentication can be easily and
unobtrusively integrated into any application or framework that supports
[Connect](http://www.senchalabs.org/connect/)-style middleware, including
[Express](http://expressjs.com/).

## Installation

    $ Yet to come

## Usage

#### Configure Strategy

The Pocket authentication strategy authenticates users using a Pocket account.  
The strategy requires a `verify` callback, which receives the
access token and username as arguments. The `verify` callback must
call `done` providing a user to complete authentication.

In order to identify your application to Pocket, specify the consumer key and callback URL within `options`.  
The consumer key and secret are obtained by [creating an application](http://getpocket.com/developer/apps/new) at
Twitter's [developer](http://getpocket.com/developer/) site.

	POCKET_CONSUMER_KEY = "Pocket consumer key";

	// Passport Set up
	var pocketStrategy = new PocketStrategy({
			consumerKey    : POCKET_CONSUMER_KEY,
			callbackURL    : "http://127.0.0.1:3000/auth/pocket/callback"
		},function(username, accessToken, done) {
			process.nextTick(function () {
				return done(null, {
					username    : username,
					accessToken : accessToken
				});
			});
		}
	);

	passport.use(pocketStrategy);

#### Authenticate Requests



## Credits

  - [Daniel Zavala](http://github.com/siedrix)

## License

    PHPBBMODDERS BEERWARE LICENSE
    version 1, may 7 2008

    this license is based on Poul-Henning Kamp 's original
    beerware license. it's been slightly modified to be more suitable for having
    in a separate file.

    as long as you keep any copyright notices and any mentions of this license
    intact (and include this file if it is a released package), you can do
    whatever you want with this stuff. if we meet one day, and you think it's
    worth it, you can buy me a beer in return.

    there is no warranty for this work, use it at your own risk.

