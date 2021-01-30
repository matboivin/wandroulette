# wandroulette

Get insulted by one man army wandre.

wandre will insult the user when they type a wrong command.

## Installation

```
curl https://raw.githubusercontent.com/matboivin/wandroulette/main/zsh.command-not-found -o /etc/zsh.command-not-found

if [ -f /etc/zsh.command-not-found ]; then
	. /etc/zsh.command-not-found
	echo "Warning /!\\ The wandre mode is activated!"
	printf "\n  $(tput bold)$(tput setaf 1)wandre:$(tput sgr0) hi ${USER} :)\n\n"
fi
```

```
if [ -f /etc/zsh.command-not-found ]; then
	if sudo rm /etc/zsh.command-not-found; then
		echo "wandre mode deactivated"
		printf "\n  $(tput bold)$(tput setaf 1)wandre:$(tput sgr0) bye ${USER} :)\n\n"
	fi
else
	echo "/etc/zsh.command-not-found doesn't exist"
fi
```

## Acknowledgements

This project is a private joke at School 42 Paris.

### Credits

This project exists thanks to hkbakke's [bash-insulter](https://github.com/hkbakke/bash-insulter).

Also based on matmutant's [zsh-insulter](https://github.com/matmutant/zsh-insulter).
