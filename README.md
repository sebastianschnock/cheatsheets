# My cheat sheets
This is my collection of cheat sheets for stuff like bash commands, shortcuts for editors, etc.

## Usage
You can define a function like this in your shell:
```
function cheatsheet {
  TYPE=$1
  PROGRAM=$2
  KEYWORD=$3
  URL=https://raw.githubusercontent.com/sebastianschnock/cheatsheets/master
  if [[ -z $KEYWORD ]]; then
    curl -s $URL/$TYPE/$PROGRAM
  else
    curl -s $URL/$TYPE/$PROGRAM | grep $KEYWORD
  fi
  echo
}

alias how='cheatsheet howto'
```

Then use it like this:
```how ssh tunnel```
