# Misc Installs
- [Gifox](https://itunes.apple.com/us/app/gifox/id1082624744?mt=12)
- [1Keyboard](https://itunes.apple.com/us/app/1keyboard/id766939888?mt=12)
- [Moom](https://itunes.apple.com/us/app/moom/id419330170?mt=12)
- [Karabiner-Elements](https://github.com/tekezo/Karabiner-Elements)
- [Pocket](https://itunes.apple.com/us/app/pocket/id568494494?mt=12)
- [1password](https://itunes.apple.com/us/app/1password-password-manager/id443987910?mt=12)
    + Syncs with iCloud
- [Node](https://nodejs.org/en/)
- [Flux](https://justgetflux.com/)
- [Rescue Time](https://www.rescuetime.com)
- [Virtual Box](https://www.virtualbox.org/)
- [Bartender](https://www.macbartender.com/)
    + [License](https://mail.google.com/mail/u/1/#inbox/158badf517ca1365)
- [Homebrew](http://brew.sh/)
    - Redis `brew install redis`
    - [jq](https://stedolan.github.io/jq/) `brew install jq`
- [Dash](https://kapeli.com/dash)
    + [License](https://mail.google.com/mail/u/0/#inbox/15b02250ecd27699)

# [Bin](https://github.com/iowillhoit/bin)
- `cd ~ && git@github.com:iowillhoit/bin.git && cd -`

# [Alfred](https://www.alfredapp.com/)
- [Enable Powerpack](https://mail.google.com/mail/u/1/#search/alfred/155282ff4b7a1391)
- Set theme
- Change trigger (command+space)
- Enable Clipboard history (Features>Clipboard)
- Sync settings (~/Dropbox/applications/alfred)
- Auto expand snippets (Features>Snippets)

# [Sublime Text 3](https://www.sublimetext.com/3)
- [Install license](https://mail.google.com/mail/u/0/#search/sublime+text/1553150d428618aa)
- Enter License `Help>Enter License`
- Clone sublime settings repo
`cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages && git clone git@github.com:iowillhoit/sublime.git .`
- [Enable `subl`](http://olivierlacan.com/posts/launch-sublime-text-3-from-the-command-line/)
    + `sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl`

# [iTerm3](https://www.iterm2.com/version3.html)
- Change "Load preferences from a custom folder or URL" to `~/Dropbox/applications/iterm`
- [Oh my zsh](https://github.com/robbyrussell/oh-my-zsh)
- [Bullet Train](https://github.com/caiogondim/bullet-train-oh-my-zsh-theme)
    + [Input Font](http://input.fontbureau.com/preview/?size=14&language=javascript&theme=solarized-dark&family=InputMono&width=400&weight=400&line-height=1.2&a=0&g=0&i=serifs_round&l=serifs_round&zero=0&asterisk=0&braces=straight&preset=default&customize=please)
- Fix Node permissions `sudo chown -R $(whoami):admin /usr/local/bin/ && sudo chown -R $(whoami):admin /usr/local/lib/`
- ? [Rupa z](https://github.com/rupa/z)
- [n](https://github.com/tj/n)
- [tldr](https://github.com/tldr-pages/tldr) `npm install -g tldr`
- [diff-so-fancy](https://github.com/so-fancy/diff-so-fancy) `brew install diff-so-fancy` -- `git config --global core.pager "diff-so-fancy | less --tabs=4 -RFX"`

## Reference
- [Key bindings](https://gist.github.com/iowillhoit/9298628129039d5e0038)

# SSH KEYS
- Link config `mkdir ~/.ssh && ln -s ~/Dropbox/applications/ssh/config ~/.ssh/config`
- Setup ssh keys `ssh-keygen -b 4096 -t rsa`

# Marketing Cloud
- `npm install -g grunt-cli && npm install -g bower && npm install -g karma-cli`
- `brew install gpg`
- If you do not have `~/.gnupg`, execute the binary `gpg` and kill the process.
- Delete any created keys `rm -f ~/.gnupg/*.gpg`
- `ln -s ~/.gnupg ~/.gpg`
- `mkdir ~/dev/platform && cd ~/dev/platform`
- `git clone git@github.exacttarget.com:ewillhoit/marketing-cloud-app.git mc-dos`
- `git clone git@github.exacttarget.com:Mobile/platform-tools.git tools`
- `unzip -j ~/dev/platform/tools/gpg/gpg.zip -d ~/.gnupg`
- `cd tools/devconnect && npm install`
- `cd ../.. && cp tools/platformapps/GitPlatformApps.sh .`
- `sh GitPlatformApps.sh`
- `cd mc-dos`
- `git remote add upstream git@github.exacttarget.com:MarketingCloudDev/marketing-cloud-app.git`
- `git fetch --all --prune`
- `git checkout -b jfv-206 upstream/jfv-206`
- `npm run setup-classic`
- `npm run setup`
- `npm start`

---
- Change `port: 3001` to `port: 3000` and `secure: true` to `secure: false` in `~/dev/platform/tools/devconnect/config/ssjsproxy.js`
- `cd Package/Dynamic/lightning-experience && npm install`
- ? `sh tools/devconnect/cert/install-cert-mac.sh`

# Misc Config
- Sign into Chrome
- [Stackato VM](http://downloads.stackato.com/vm/v3.4.2/)
- [Hide Cisco](https://www.cnet.com/news/prevent-an-applications-dock-icons-from-showing-in-os-x/)
    - Add to plist
    ```
    <key>LSUIElement</key>
    <true/>
    ```
- Turn on dictation
    - System Preferences>Accessibility>Speech
    - Serena @ 60% rate
    - Check "Speak selected text when the key is pressed"
- [Non-native fullscreen support (sorta)](https://apple.stackexchange.com/a/146951)

# TODO
- Create github pusher
    + `~/bin`
    + `~/Library/Application\ Support/Sublime\ Text\ 3/Packages`
    + `~/Library/Application\ Support/Alfred\ 3`
- [Redis Launchd](http://naleid.com/blog/2011/03/05/running-redis-as-a-user-daemon-on-osx-with-launchd)
- login script `tldr --update`
- save alfred settings to repo
    + ignore:
        * license.plist
        * usage.data
        * Databases/clipboard.alfdb.data
- backup Input font

