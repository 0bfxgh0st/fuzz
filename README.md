# FUZZ

```
Usage fuzz -u <url> -w <wordlist>

Options:

      -u                        : Specify a URL for the request
      -w                        : Specify a wordlist file
      -c                        : Colored output
      --hc/hl/hw/hh N[,N]+      : Hide responses with the specified code/lines/words/chars
      --sc/sl/sw/sh N[,N]+      : Show responses with the specified code/lines/words/chars

Example: 

      fuzz -c -u http://ghost.server/FUZZ -w /usr/share/wordlists/dirb/common.txt --sc=200,403,500
```      

```
┌──(root💀ghost)-[/home/ghost]
└─# fuzz -u http://ghost.server/FUZZ -w /usr/share/wordlists/dirb/common.txt -c --hc=404,403

   ___                           
 /'___\                          
/\ \__/  __  __  ____    ____     by 0bfxgh0st*
\ \ ,__\/\ \/\ \/\_ ,`\ /\_ ,`\   && D3Ext
 \ \ \_/\ \ \_\ \/_/  /_\/_/  /_ 
  \ \_\  \ \____/ /\____\ /\____\
   \/_/   \/___/  \/____/ \/____/  
   

Target: http://ghost.server/FUZZ
Total requests: 4614

============================================================================
ID           Response        Lines       Words      Chars           Payload
============================================================================

1              200            368         933        10701          ""
290            200            1           1          5              "admin.php"
2020           200            368         933        10701          "index.html"
3588           200            126         355        7173           "server-status"

Total time: 4.047680139541626
```
