MODES:
◦	Router> – USER prompt mode
◦	Router# – PRIVILEGED EXEC prompt mode
◦	Router(config) – terminal configuration prompt
◦	Router(config-if) – interface configuration prompt
◦	Router(config-subif) – sub-interface configuration prompt

Configuring Commands
-	Router(config)# hostname shreyas
-	Router(config-if) no shut
-	Router(config-if) shut

Set Banner to Router
-	Router(config) banner login (telnet). “welcome to hpes .”
-	Router(config) banner motd. (message of the day Banner)

Setting Router Password
-	Router(config) line console 0
-	Router(config-line) password hpes
-	Router(config-line) login

Set administrative mode Password
-	Router(config) enable password hpes
-	Router(config) enable secret hpes

Set Telnet Mode Passwords
-	Router(config) line vty 0 4
-	Router(config-line) password hpes
-	Router(config-line) login
