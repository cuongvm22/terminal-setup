## MacOS X + oh my zsh + powerline fonts + visual studio code (vscode) terminal settings
> Thank you everybody, Your comments makes it better

### Install oh my zsh
http://ohmyz.sh/

```sh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Install powerline fonts
https://github.com/powerline/fonts

### download agnoster theme
https://github.com/mbadolato/iTerm2-Color-Schemes/zipball/master

### change setting for vs code
```sh
"terminal.integrated.fontFamily": "Source Code Pro for Powerline",
"terminal.integrated.shell.osx": "/bin/zsh"

// @ChongTang, @ramonsantos added
// "terminal.integrated.fontFamily": "Hack Nerd Font"

// @dalekurt added (belows which gives me the the fonts for the terminal and the icons from Nerd Font.)
// "terminal.integrated.fontFamily": "'Source Code Pro for Powerline', 'Hack Nerd Font'

// @kaustuv added
// after the changing the font, still had some issues with the glyph spacing in the integrated terminal - fixed it with 
// "terminal.integrated.rendererType": "canvas"
```

1. change theme for Mac OSX Terminal to agnoster
1. add DEFAULT_USER=`whoami` in `~/.zshrc`
1. change theme to `agnoster` in `~/.zshrc`
