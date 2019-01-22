# Slack Night Mode
A user style for easy Slack theming. [CC0](http://creativecommons.org/publicdomain/zero/1.0/).

![Black Screenshot](https://userstyles.org/style_screenshots/117475_after.png)


## Usage

### Desktop App

Find your Slack's application directory.

    Windows: %homepath%\AppData\Local\slack\
    Mac: /Applications/Slack.app/Contents/
    Linux: /usr/lib/slack/ (Debian-based)

Open up the following file *resources/app.asar.unpacked/src/static/ssb-interop.js* and at the very bottom, add

```javascript 
document.addEventListener('DOMContentLoaded', function() {
$.ajax({
  url: 'https://raw.githubusercontent.com/vumik/slack-night-mode/master/css/raw/black.css',
  success: function(css) {
    $("<style></style>").appendTo('head').html(css);
  }
});
});
```

That's it! Restart Slack and see how well it works.

**Important**: You'll have to do this every time Slack updates.


### Browser

This theme requires that you use [a user styles extension](https://github.com/openstyles/stylus/wiki/Stylish-Alternatives) for your browser, such as Stylus (available for [Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/), [Chrome](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne), and [Opera](https://addons.opera.com/en/extensions/details/stylus/)).

