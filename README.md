# dotfiles

### How to use

clone the repository:

```bash
$ git clone https://malbolge.dev.br/malbolge/dotfiles.git
```

After that, you must change the branch to the main, as it comes in the master branch.

```bash
$ git checkout main
```

This repository contains several different types of *dotfiles*. To use it you should source the appropriate content into the desired .conf file.

## .tmux.conf

---

If you want to use the *.tmux.conf* configuration file, you must *source* it into the *.tmux.conf* present in the home folder (the actual file that the *tmux* will read, if it's not present, just ``` touch .tmux.conf```), like so:

```bash
$ echo "source-file <path>/dotfiles/.tmux.conf" >> ~/.tmux.conf
```



## .zsh

----

In a similar way, the zsh *dotfiles* should be sourced into the .zshrc, present in the home folder.

If you are using a framework such as [ohmyzsh](https://github.com/ohmyzsh/ohmyzsh), you must pay attention to where to source it into the file.

Look for the following line:

```shell
# User configuration
source $ZSH/oh-my-zsh.sh
...
```

And put your source right bellow this line, like so:

```shell
source <path>/dotfiles/.zsh-alias.zsh
```

If you're not using anything, just:

```shell
$ echo "<path>/dotfiles/.zsh-alias.zsh" >> ~/.zshrc
```

Just change the \<path\> string to the path that you cloned the repository into.



