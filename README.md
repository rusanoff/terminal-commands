# Terminal Commands
MacOS Terminal Commands

### Добавить разделитель в Dock:

```bash
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="spacer-tile";}'
```

Затем:

```bash
killall Dock
```

***

### Убить процесс какого-нибудь порта:

Создать функцию в файле `.zshrc`

```bash
killport() {
    kill -9 $(lsof -i:"$1" -t) 2> /dev/null
}
```

Затем:

```bash
killport ${PORT_NUMBER}
```

***

### Запуск Google Chrome с отключенной безопасностью

```bash
open -n -a /Applications/Google\ Chrome.app --args --disable-web-security --user-data-dir=/Users/${USER_NAME}/.config/chrome-dev
```
