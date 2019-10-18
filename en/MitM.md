TOPIC: MitM
AUTHORS: Teoli; teoli@mozilla.net; mdn:teoli
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz

# MitM

A **Man-in-the-middle attack** (MitM) intercepts a communication between two systems. For example,
a Wi-Fi router can be compromised.

Comparing this to physical mail: If you're writing letters to each other, the mailman can intercept
each letter you mail. They open it, read it, eventually modify it, and then repackage the letter
and only then send it to whom you intended to sent the letter for. The original recipient would then
mail you a letter back, and the mailman would again open the letter, read it, eventually modify it,
repackage it, and give it to you. You wouldn't know there's a man in the middle in your communication
channel – the mailman is invisible to you and to your recipient.

In physical mail and in online communication, MITM attacks are tough to defend. A few tips:

- Don't just ignore certificate warnings. You could be connecting to a phishing server
or an imposter server.

- Sensitive sites without HTTPS encryption on public Wi-Fi networks aren't trustworthy.

- Check for HTTPS in your address bar and ensure encryption is in-place before logging in.

## Learn More

- OWASP Article: [Man-in-the-middle attack](https://www.owasp.org/index.php/Man-in-the-middle_attack)
- Wikipedia: [Man-in-the-middle attack](https://www.owasp.org/index.php/Man-in-the-middle_attack)
- The [`Public-Key-Pins`](https://wiki.developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Public-Key-Pins)
header (HPKP) can significantly decrease the risk of MITM by instructing browsers to -require a
whitelisted certificate for all subsequent connections to that website.
