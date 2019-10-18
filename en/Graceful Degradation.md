TOPIC: Graceful Degradation
AUTHORS: Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills

# Graceful Degradation

**Graceful degradation** is a design philosophy that centers around trying to build a modern web
site/application that will work in the newest browsers, but fall back to an experience that while
not as good still delivers essential content and functionality in older browsers.

Polyfills can be used to build in missing features with JavaScript, but acceptable alternatives to
features like styling and layout should be provided where possible, for example by using theCSS cascade,
or HTML fallback behaviour. Some good examples can be found in Handling common HTML and CSS problems.

It is a useful technique that allows Web developers to focus on developing the best possible websites,
given that those websites are accessed by multiple unknown user-agents. Progressive enhancement is
related but different — often seen as going in the opposite direction to graceful degredation.
In reality both approaches are valid and can often complement one another.

## Learn More

## General Knowledge

- [Graceful degradation](https://en.wikipedia.org/wiki/Graceful%20degradation) on Wikipedia
