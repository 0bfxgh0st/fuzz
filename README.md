# FUZZ

```
Usage python3 fuzz -u <url> -w <wordlist>

Options:

      -u       url
      -w       wordlist
      --sc     show code status
      --hc     hide code status

Example: 

      python3 fuzz -u http://ghost.server/index.php?FUZZ=/etc/passwd -w /usr/share/wordlists/dirb/common.txt --sc=200,403,500
```      

```
┌──(root💀ghost)-[/home/ghost]
└─# python3 fuzz -u http://ghost.server/index.php?page=/etc/FUZZ -w /usr/share/wordlists/dirb/common.txt --hc=500

   ___                           
 /'___\                          
/\ \__/  __  __  ____    ____     by 0bfxgh0st*
\ \ ,__\/\ \/\ \/\_ ,`\ /\_ ,`\   && D3Ext
 \ \ \_/\ \ \_\ \/_/  /_\/_/  /_ 
  \ \_\  \ \____/ /\____\ /\____\
   \/_/   \/___/  \/____/ \/____/  
   

Target: http://ghost.server/index.php?page=/etc/FUZZ
Total requests: 4614

============================================================================
ID           Response        Lines       Words      Chars           Payload
============================================================================

1103           200            22          190        1042           "crontab"
1471           200            14          81         653            "environment"
1835           200            83          83         1241           "group"
1921           200            7           23         197            "hosts"
2122           200            2           5          30             "issue"
2400           200            3           19         111            "magic"
2567           200            5           36         195            "modules"
2578           200            7           40         282            "motd"
2866           200            53          83         3103           "passwd"
3160           200            34          111        769            "profile"
3449           200            40          117        887            "rpc"
3591           200            361         1773       12813          "services"
```
