# OAuth by FriendsOfFlarum

![License](https://img.shields.io/badge/license-MIT-blue.svg) [![Latest Stable Version](https://img.shields.io/packagist/v/fof/oauth.svg)](https://packagist.org/packages/fof/oauth) [![OpenCollective](https://img.shields.io/badge/opencollective-fof-blue.svg)](https://opencollective.com/fof/donate) [![Donate](https://img.shields.io/badge/donate-datitisev-important.svg)](https://datitisev.me/donate)


A [Flarum](http://flarum.org) extension. Allow users to log in with GitHub, Twitter, Facebook, Discord, GitLab, Google and LinkedIn!

### Installation

```sh
composer require fof/oauth:"*"
```

### Updating

```sh
composer update fof/oauth
```


### Configuration

#### Translation

You can replace the text for the forum sign in buttons in two ways.
- Use `fof-oauth.forum.providers.<name>` to replace the name of the provider on the forum side
- Use `fof-oauth.forum.log_in.with_<name>_button` to replace the entire button "Log In with <name>" text

### Extending

It is possible to add additional `Providers` using an extender. See [OAuth-Microsoft](https://github.com/imorland/flarum-ext-oauth-microsoft) for an example of how to accomplish this but basically:

- In your new extension, require `fof/oauth` as a dependency
- Define a new `Provider` which extends `FoF\OAuth\Provider`
- From your new extensions `extend.php`, register the provider `(new FoF\OAuth\Extend\RegisterProvider(MyNewProvider::class))`
- Provide the required translations under the `fof-oauth` namespace. See the linked example extension for details on which keys are required.
- (optionally) Provide an admin panel link to `fof/oauth` for easy configuration. Again, see the linked example.
- (optionally) Provide any CSS required to style your new login button. See the linked example.

### Links

[![OpenCollective](https://img.shields.io/badge/donate-friendsofflarum-44AEE5?style=for-the-badge&logo=open-collective)](https://opencollective.com/fof/donate) [![GitHub](https://img.shields.io/badge/donate-datitisev-ea4aaa?style=for-the-badge&logo=github)](https://datitisev.me/donate/github)

- [Discuss](https://discuss.flarum.org/d/25182)
- [Packagist](https://packagist.org/packages/fof/oauth)
- [GitHub](https://github.com/FriendsOfFlarum/oauth)

An extension by [FriendsOfFlarum](https://github.com/FriendsOfFlarum).
