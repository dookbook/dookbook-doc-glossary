TOPIC: SMTP
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         T. Uemura; Uemmra3@gmail.com; github:Uemmra3
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Teoli; teoli@mozilla.net; mdn:teoli

# SMTP

**SMTP** (Simple Mail Transfer Protocol) is a protocol used to send a new email.
Like POP3 and NNTP, it is a state machine-driven protocol.

The protocol is relatively straightforward. Primary complications include supporting various
authentication mechanisms ([GSSAPI](http://en.wikipedia.org/wiki/Generic_Security_Services_Application_Program_Interface),
[CRAM-MD5](http://en.wikipedia.org/wiki/CRAM-MD5),
[NTLM](http://en.wikipedia.org/wiki/NTLM), MSN, AUTH LOGIN,
AUTH PLAIN, etc.), handling error responses, and falling back when authentication mechanisms fail
(e.g., the server claims to support a mechanism, but doesn't).
