# Pushover.net plugin for irssi

Simple enough: when your highlights are triggered, send a notification to you on [Pushover][pushover].

Currently the sole distinguishing feature of this plugin is that it forks before sending, because on my tiny low-power ARM server sending the notification blocked just enough to annoy me.

Requires `LWP::UserAgent`. If you don't have it, try something like `sudo apt-get install libwww-perl`.

## Install

Let's face it, if you're the sort of person who's using irssi you probably already know this, but:

Install it by putting it into `~/.irssi/scripts/`

If you want it to automatically run, symlink the script into `~/.irssi/scripts/autorun/`

## Configuration

You have to provide a user token for messages to be sent to. It's on your [dashboard][pushover].

`/set pushover_user = [token here]`

If you want to use your own application key, make one in your dashboard and then do:

`/set pushover_app = [token here]`

You can make sure it's working by going:

`/pushover send This is a test message`

[pushover]: http://pushover.net/
