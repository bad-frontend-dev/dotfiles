autoload -Uz compinit
compinit -d ~/.cache/zcompdump

zstyle ':completion:*:*:*:*:*' menu select
zstyle ':completion:*' auto-description 'specify: %d'
zstyle ':completion:*' completer _expand _complete
zstyle ':completion:*' format 'Completing %d'
zstyle ':completion:*' group-name ''
zstyle ':completion:*' list-colors ''
zstyle ':completion:*' list-prompt %SAt %p: Hit TAB for more, or the character to insert%s
zstyle ':completion:*' matcher-list 'm:{a-zA-Z}={A-Za-z}'
zstyle ':completion:*' rehash true
zstyle ':completion:*' select-prompt %SScrolling active: current selection at %p%s
zstyle ':completion:*' use-compctl false
zstyle ':completion:*' verbose true
zstyle ':completion:*:kill:*' command 'ps -u $USER -o pid,%cpu,tty,cputime,cmd'

HISTFILE=~/.histfile
HISTSIZE=1000
SAVEHIST=1000

if uwsm check may-start && uwsm select; then
	exec systemd-cat -t uwsm_start uwsm start hyprland
fi

bindkey "^[[1;3C" forward-word
bindkey "^[[1;3D" backward-word
bindkey "^[[1;5C" forward-word
bindkey "^[[1;5D" backward-word

PS1="[%n@%M %1~]$ "

daysuntil() {
	echo $((($(date +%s --date $1)-$(date +%s))/(3600*24))) days
}

#alias ssh="kitten ssh"
alias ls="ls --color"
alias s="ssh cob@ssh.kittycob.dev -p 9000"
alias z="nvim ~/.zshrc"
alias h="nvim ~/.config/hypr/hyprland.conf"
alias cp="cp -v"

export MANPAGER="nvim +Man!"
