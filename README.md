# my cheat sheets
This is my collection of cheat sheets for stuff like bash commands, shortcuts for editors, etc.

## folders
- howto: general tips and howto instructions
- keys: shortcuts

## usage
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

alias keys='cheatsheet keys'
alias howto='cheatsheet howto'
```

Then use it like this:
```keys sublime'''
or:
```howto ssh tunnel```