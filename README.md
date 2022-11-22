## FUZZ

```
Usage fuzz -u <url> -w <wordlist>

Options:

      -u                        : Specify a URL for the request
      -w                        : Specify a wordlist file
      -c                        : Colored output
      -H                        : Use header (ex:"Host: FUZZ.ghost.server")
      --hc/hl/hw/hh N[,N]+      : Hide responses with the specified code/lines/words/chars
      --sc/sl/sw/sh N[,N]+      : Show responses with the specified code/lines/words/chars

Examples: 

      fuzz -c -u http://ghost.server/FUZZ -w /usr/share/wordlists/dirb/common.txt --sc=200,403,500
      fuzz -u http://ghost.server/ -w /usr/share/wordlists/dirb/common.txt -c -H 'Host: FUZZ.ghost.server' --hw=933,35
```
