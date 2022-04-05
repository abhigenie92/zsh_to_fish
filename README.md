# zsh_to_fish
How to make zsh like fish?


1. Install oh-my-zsh
```
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

2. Clone necessary plugins.
```
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

3. Add plugins to `~/.zshrc` as
```
plugins = ( [plugins...] zsh-autosuggestions history-substring-search zsh-syntax-highlighting)
```
Note: make sure zsh-syntax-highlighting is the last one in the above list.

4. Fix background theme issues(, not necessary depends on your theme.)
Add the following line to your `~/.zshrc`.
```
ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=white'
```

5. Restart zsh
```
source ~/.zshrc
```
