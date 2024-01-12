This is an informal audit of a word list sent to me.

## List Attributes

Here's what my [Word List Auditor tool](https://github.com/sts10/wla) found:

```text
Lines found               : 7779
Free of exact duplicates  : true
Free of fuzzy duplicates  : true
Free of blank lines       : true
Unique words found        : 7779
No start/end whitespace   : true
No non-ASCII characters   : true
Unicode normalized        : true
Free of prefix words      : false
Free of suffix words      : false
Uniquely decodable        : false
Above brute force line    : true
Length of shortest word   : 4 characters (thug)
Length of longest word    : 8 characters (zucchini)
Mean word length          : 6.42 characters
Entropy per word          : 12.925 bits
Efficiency per character  : 2.013 bits
Assumed entropy per char  : 3.231 bits
Shortest edit distance    : 1
Mean edit distance        : 6.197
Longest shared prefix     : 7
Unique character prefix   : 8
```

This mostly seems find. 

However one thing of note is that it found a "Longest shared prefix" of 7. This means that at least two words have the same first 7 letters. Using [Tidy](https://github.com/sts10/tidy), I found some pairs of words on the list that share a 5-letter prefix: 

```text
carefree,careful
convey,convex
leather,leathery
sloth,slothful
swing,swingy
unheard,unheated
```

So for example, a program could not execute an auto-complete if the user typed "conve" or "swing".

## Potential homophones

Again using Tidy, I found a number of pairs of homophones (or near homophones) that both appear on the list.
```text
accept,except
addition,edition
affect,effect
ashore,assure
banner,banter
batty,baddie
bidder,bitter
bobble,bauble
borough,burgh
breach,breech
caller,collar
callous,callus
cannon,canon
carve,calve
catty,caddie
century,sentry
chock,chalk
chute,shoot
click,clique
coating,coding
cookie,kooky
coral,choral
diffuse,defuse
gofer,gopher
gonna,gunner
hallow,hollow
hiccough,hiccup
holler,hauler
khaki,cocky
kiddy,kitty
knotty,naughty
ladder,latter
leader,liter
lichen,liken
loaner,loner
looney,loony
marry,merry
mucous,mucus
parish,perish
pauper,popper
pleural,plural
proceed,precede
rapper,wrapper
rider,writer
shudder,shutter
taper,tapir
tender,tinder
tremor,trimmer
waist,waste
whither,wither
```

## British or uncommon word spellings
Here's a list of words that probably have different, more common spellings in the US ("dialog", "glamor", "skillful"). Of course if you're aiming the list for British users, that'd be fine! 
```text
bogeyman
chastise
dialogue
epilogue
glamour
idyll
mould
skilful
sledge
sulphur
useable
```

