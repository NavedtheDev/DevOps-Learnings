* Use # to add a comment. 

* The 'echo' command has a -e option, with which we can provide a color code. Example,

```
echo -e "\033[0;32mInstalling firewalld...\033[0m"
```

* We can also assign color codes to a variable. Example,

```
GREEN="\033[0;32m"
NC="\033[0m"

echo -e "${GREEN}Installing firewalld...${NC}"
```

* We can also create functions for using colors. Example,

```
function print_color() {
    GREEN="\033[0;32m"
    NC="\033[0m"

echo -e "${GREEN} $1 ${NC}"
}
```
