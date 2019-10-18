TOPIC: Network Throttling

# Network Throttling

**Network throttling** is an intentional slowing down of internet speed. In web performance,
network throttling, or network condition emulation, it is used to emulate low bandwidth conditions
experienced by likely a large segment of a site's target user base.

It’s important not to overlook network conditions users experience on mobile. The internet speeds
for developers creating web applications in a corporate office building on a powerful computer are
generally very fast. As a developer, tech writer, or designer, this is likely your experience.
The network speeds of a mobile user accessing that web application, possibly while traveling or in
a remote area with poor data plan covereage, will likely be very slow, if they are able to get
online at all. Network throttling enables a developer to emulate an experience of a user.
Most browser developer tools, such as the browser inspector, provide a function to emulate different
network conditions. By emulating your user's experience via network throttling, you can
more readily identify and fix load time issues.

In a browser's developer tools, under the network panel, there is generally a drop down
list with network speed options including wifi, good 3G, 2G, etc., with a default value
of "no throttling".  You can even test 'offline'.

## See Also

- [Synthetic monitoring](https://wiki.developer.mozilla.org/en-US/docs/Glossary/Synthetic_monitoring)
