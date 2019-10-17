TOPIC: Challenge-response Authentication
AUTHORS: Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Teoli; teoli@mozilla.net; mdn:teoli

# Challenge-response Authentication

In security protocols, a challenge is some data sent to the client by the server in order to
generate a different response each time. Challenge-response protocols are one way to fight against
[replay attacks](https://en.wikipedia.org/wiki/Replay_attack) where an attacker listens to the previous
messages and resends them at a later
time to get the same credentials as the original message.

The HTTP authentication protocol is challenge-response based, though the "Basic" protocol
isn't using a real challenge (the realm is always the same).

## Learn More

- [challenge-response authentication](https://en.wikipedia.org/wiki/Challenge%E2%80%93response_authentication)
on Wikipedia.
