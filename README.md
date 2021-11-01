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

### Выгрузить проект с удаленного хоста:

```bash
rsync —progress -avhz —delete-after login@host:/project_dir/ /local_project_dir/
```

***

### Загрузить проект на удаленный хост

```bash
rsync —progress -rlpgoDvhz —delete-after /local_project_dir/ login@host:/project_dir/
```

***
