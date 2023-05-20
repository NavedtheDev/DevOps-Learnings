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

print_color "Installing firewalld..."
```

* Example of a function to use multiple colors, 

```
function print_color() {

    case $1 in 
      "green") COLOR="\033[0;32m" ;;
      "red") COLOR="\033[0;31m" ;;
      "*") COLOR="\033[0m"
    esac

    echo -e "${COLOR} $2 ${NC}"
}

print_color "green" "Installing firewalld..."
print_color "red" "Failed!"
```
