# wandroulette

<p align="center">
  <img src="assets/evildog.png" alt="dog pic" />
</p>

Get insulted by one man army wandre.

wandre will insult the user when they type a wrong command.

:warning: This project is a private joke at School 42 Paris.

## Get wandred!

Done for zsh to be used at school 42 or inside 42's VM.  
Bash compatible (TODO: update the readme).

### Oh yeah insult me wandre

1. Get the file.

```console
# Method 1
curl https://raw.githubusercontent.com/matboivin/wandroulette/main/zsh.command-not-found -o /etc/zsh.command-not-found

# Method 2
git clone https://github.com/matboivin/wandroulette.git
sudo cp wandroulette/zsh.command-not-found /etc/
```

2. Add the following lines to your `.zshrc` file:

```sh
# wandre mode

if [ -f /etc/zsh.command-not-found ]; then
	. /etc/zsh.command-not-found
	echo "Warning /!\\ The wandre mode is activated!"
	echo "\n  $(tput bold)$(tput setaf 1)wandre:$(tput sgr0) hi ${USER} :)\n"
fi
```

The `# wandre mode` comment is here to find these lines again more easily if needed.

3. Source your `.zshrc` file. In your terminal, run:

```console
source ~/.zshrc
```

### Stop it wandre!

In your terminal, run:

```sh
if [ -f /etc/zsh.command-not-found ]; then
	if sudo rm /etc/zsh.command-not-found; then
		echo "wandre mode deactivated"
		echo "\n  $(tput bold)$(tput setaf 1)wandre:$(tput sgr0) bye ${USER} :)\n"
	fi
else
	echo "/etc/zsh.command-not-found doesn't exist"
fi
```

## Acknowledgements

crebert for the wonderful "Get wandred" pun.  
wandre for the legendary RTFM attitude.

### Credits

This project exists thanks to hkbakke's [bash-insulter](https://github.com/hkbakke/bash-insulter).

Also based on matmutant's [zsh-insulter](https://github.com/matmutant/zsh-insulter).
