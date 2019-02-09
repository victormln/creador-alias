Si no sabes que es un alias, te recomiendo que los utilices. Puedes ver el enlace en la wikipedia para saber porque son útiles: <a href="https://en.wikipedia.org/wiki/Alias_(command)" target="_blank">¿Qué és un alias?</a>
___

# Malias

Malias is a shell script that let's you to add, edit, delete and more to manage your aliases on linux/mac. It's compatible with bash and zshrc (or either use your own file).

Example to show your current aliases.
```shell
malias -l
```

## Installation

```shell
git clone https://github.com/victormln/alias.git ~/.alias
~/.alias/install.sh
source ~/.bashrc   # or source ~/.zshrc
```

The install script creates required default configs and adds the following line to your .bashrc or .zshrc:

```shell
alias malias="~/.alias/alias.sh"
```

**Note:** To uninstall you can use in your console:
```shell
uninstall_malias
```

## Configuration


You can configure a lot of paramaters. For example, don't search for automatic updates, change the language or change the directory of the file that contains your aliases. To change all this parameters you can open the file user.conf.

## Use

For example, if you want to add an alias, you can execute:
```shell
malias -a your_alias
```

All arguments available:

|Argument           |Abbreviation|Meaning                                   |Use|
| ------------- | ---- | ---------------------------------------- |----------|
|`--help`       |`-h`     | Show available commands         |`malias --help`  |
|`list` or `view` or `show` |`-l`  | Show the aliases you have             |`malias -l`    |
|`add`     |`-a`  | Add an alias (or more than one)   |`malias -a test1`      |
|`edit`     |`-e`  | Edit an alias (or more than one)   |`malias -e test1`      |
|`delete`     |`-d`  | Delete an alias (or more than one)   |`malias -d test1 test2`      |
|`copy`     |`-cp`  | Copy an alias (or more than one). You can copy an alias that already exists.   |`malias -cp alias_origen alias_nuevo alias_nuevo2`      |
|`--conf`     |  | Open the file with all the configurations. By default the file is opened with "vi", you can change it in the opened file.  |`malias --conf`      |.
|`--clear`     |  | Remove from the file that contains the aliases, those that are empty and empty lines  |`malias --clear`      |
|`--import`     |  | Import alises from specific file.  |`malias --import directory/fileName.txt`      |
|`install`     |  | Install an aliases from the directory "alias".  |`malias install deliverea`      |
|`--restore`     |  | Restore a backup file with all your aliases before executing any action.  |`malias --restore`      |
|`--update`     |  | Search for available updates.  |`malias --update`      |
|     |`-v`  | Shows the version of the script.  |`malias -v`      |
