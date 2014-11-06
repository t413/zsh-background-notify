# zsh-background-notify

cross-platform background notifications for long running commands! Supports OSX and Ubuntu linux.

----------------------------------

## How to use!

If you're already running [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh), no problem! just clone the repository and add one line your `.zshrc`:

~~~ sh
git clone https://github.com/t413/zsh-background-notify.git ~/.zsh-background-notify
echo 'source $HOME/.zsh-background-notify/bgnotify.plugin.zsh' >> ~/.zshrc
~~~

- On OS X you'll need [terminal-notifer](https://github.com/alloy/terminal-notifier)
  * `brew install terminal-notifier` (or `gem install terminal-notifier`)
- On ubuntu you're already all set!


## How it works

In zsh you can add a user-hook `preexec` that runs before executing a command and `precmd` that runs just before re-prompting. Timing the difference between them gives you execution time!

To check if you're in the background we can use xprop to find the NET_ACTIVE_WINDOW in ubuntu and osascript to run a simple apple script to get the same thing (although slower).


## Alternatives:

Here are a few similar alternatives, most are platform spesific however.

- This [reddit post](http://www.reddit.com/r/linux/comments/1pooe6/zsh_tip_notify_after_long_processes/)
- [zsh-notify](https://github.com/marzocchi/zsh-notify) plugin for Mac OS X
- [dotzsh notify](https://github.com/dotphiles/dotzsh/tree/master/modules/notify)
- [zbell](https://gist.github.com/jpouellet/5278239)
