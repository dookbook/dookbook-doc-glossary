TOPIC: Random Number Generator
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Teoli; teoli@mozilla.net; mdn:teoli

# Random Number Generator

A **PRNG** (pseudorandom number generator) is an algorithm that outputs numbers in a
complex, seemingly unpredictable pattern. Truly random numbers (say, from a radioactive
source) are utterly unpredictable, whereas all algorithms are predictable, and a PRNG
returns the same numbers when passed the same starting parameters or seed.

PRNGs can be used for a variety of applications, such as games.

A cryptographically secure PRNG is a PRNG with certain extra properties making it
suitable for use in cryptography. These include:

- that it's computationally unfeasible for an attacker (without knowledge of the seed)
to predict its output
- that if an attacker can work out its current state, this should not enable the
attacker to work out previously emitted numbers.

Most PRNGs are not cryptographically secure.

## Learn More

### General Knowledge

- [Pseudorandom Number Generator](https://en.wikipedia.org/wiki/Pseudorandom%20number%20generator)
on Wikipedia
- [`Math.random()`](https://wiki.developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random),
a built-in JavaScript PRNG function. Note that this is not a cryptographically
secure PRNG.
- [`Crypto.getRandomValues()`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Crypto/getRandomValues):
this is intended to provide cryptographically secure numbers.
