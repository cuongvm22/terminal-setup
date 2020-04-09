## MacOS X + oh my zsh + powerline fonts + visual studio code (vscode) terminal settings
> Thank you everybody, Your comments makes it better

### Install oh my zsh
http://ohmyz.sh/

```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Install powerline fonts
https://github.com/powerline/fonts

### or Install Nerd Fonts.
https://www.nerdfonts.com/font-downloads

### Download agnoster theme
https://github.com/mbadolato/iTerm2-Color-Schemes/zipball/master

### Change settings for vscode
```sh
"terminal.integrated.fontFamily": "Source Code Pro for Powerline",
"terminal.integrated.shell.osx": "/bin/zsh"

// @Drakal added
// I'd also consider adjusting line height if icons are cut off on top too or things look super cramped.
// "terminal.integrated.lineHeight": 1.3

// @ChongTang, @ramonsantos added
// @gaochundong said it works like a charm.
// "terminal.integrated.fontFamily": "Hack Nerd Font"

// @dalekurt added (belows which gives me the the fonts for the terminal and the icons from Nerd Font.)
// "terminal.integrated.fontFamily": "'Source Code Pro for Powerline', 'Hack Nerd Font'

// @nickhingston , @olivebay added for powerlevel10k
// I use powerline10k - which uses https://github.com/romkatv/powerlevel10k/#recommended-meslo-nerd-font-patched-for-powerlevel10k
// so this worked for me:
// "terminal.integrated.fontFamily": "MesloLGS NF" 

// @kaustuv added
// after the changing the font, still had some issues with the glyph spacing in the integrated terminal - fixed it with 
// @ar2zee : fixed the problem for me.
// "terminal.integrated.rendererType": "canvas"
```

1. Change Theme for Mac OSX Terminal to agnoster
1. Add DEFAULT_USER=`whoami` in `~/.zshrc`
1. Change Theme to `agnoster` in `~/.zshrc`
