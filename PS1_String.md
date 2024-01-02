```shell
export PS1='[\[\e[38;5;53;1m\]\u\[\e[0m\]@\[\e[38;5;124;1m\]\h \[\e[0m\]$? \[\e[93m\]\w \[\e[94m\]\d \[\e[32;1;5m\]\T\[\e[0m\]]\$ '
```


```shell
## PS1 string with newline.
export PS1='[\[\e[38;5;53;1m\]\u\[\e[0m\]@\[\e[38;5;124;1m\]\h \[\e[0m\]$? \[\e[93m\]\w \[\e[94m\]\d \[\e[32;1;5m\]\T\[\e[0m\]]\n\$'
```

```shell
## PS1 string with multiple elements.
PROMPT_COMMAND='PS1_CMD1=$(ip route get 1.1.1.1 | awk -F"src " '"'"'NR == 1{ split($2, a," ");print a[1]}'"'"')'; PS1='[\[\e[38;5;53;1m\]\u\[\e[0m\]@\[\e[38;5;124;1m\]\h \[\e[0m\]$? \[\e[93m\]\w \[\e[94m\]\d \[\e[32;1;5m\]\T \[\e[0m\]${PS1_CMD1} \s \l \W \w \H \@ \T \t \D{}]\n\$ '
```
