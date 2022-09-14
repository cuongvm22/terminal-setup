## MacOS X + oh my zsh + powerline fonts + visual studio code (vscode) terminal settings
> Thank you everybody, Your comments makes it better

### Install oh my zsh
http://ohmyz.sh/

```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Install powerline fonts
https://github.com/powerline/fonts

### or Install Nerd Fonts. (If you don't use powerline fonts)
https://www.nerdfonts.com/font-downloads
> recommend font: Hack Nerd Font https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/Hack.zip

### Oh my zsh plugin
1. zsh-autosuggestions
```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

2. zsh-syntax-highlighting
```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
- plugins=(git zsh-autosuggestions zsh-syntax-highlighting)

### Change settings for vscode

1. open vscode
2. open Command Pallete (Short Cut: `F1`)
3. type `settings` and Select `Preferences: Open Settings (JSON)`
4. Add or Edit below settings to Settings JSON file
5. Save.
6. That's all 

ps. This JSON type is `JSON with Comments`, so you can use comment syntax in it. 

```sh
"terminal.integrated.fontFamily": "Source Code Pro for Powerline",
// @vtwang added (deprecated)
// "terminal.integrated.shell.osx": "/bin/zsh",
"terminal.integrated.defaultProfile.osx": "zsh",

// @jasonekratz added
// This fixed the glyph issues I was having with Inconsolata Nerd Font.
"terminal.integrated.gpuAcceleration": "canvas",

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
// (deprecated)
// "terminal.integrated.rendererType": "canvas"
```

### Change Theme for Mac OSX Terminal to agnoster

1. Add DEFAULT_USER=`whoami` in `~/.zshrc`
1. Change Theme to `agnoster` in `~/.zshrc`
1. Restart Terminal or `source ~/.zshrc` 


### Download `agnoster` theme and set up

1. Download https://github.com/mbadolato/iTerm2-Color-Schemes/zipball/master
2. Unzip
3. Open Mac Terminal
4. `CMD` + `,` open settings
5. on Left Sidebar, Click `Config` Icon and Select `Import...` 
6. Choose Terminal Schema: `UnzipPath/terminal/*.terminal`
7. I recommend `Solarized Dark.terminal` 
8. then, make it default (select imported schema and click "Default" button below)
9. That'all. if you restart terminal, you can see great `agnoster` theme with oh my zsh.


