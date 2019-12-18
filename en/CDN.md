TOPIC: Content Delivery Network

# Content Delivery Network (CDN)

A **CDN** (**Content Delivery Network**) is a group of servers spread out over many locations.
These servers store duplicate copies of data so that servers can fulfill data requests based on
which servers are closest to the respective end-users.
CDNs make for fast service less affected by high traffic.

CDNs are used widely for delivering stylesheets ([[CSS]]) and [[JavaScript]] files (**static assets**)
of libraries like *Bootstrap*, *jQuery* etc.
Using CDN for those library files is preferable for a number of reasons:

- Serving libraries' static assets over CDN *lowers the request burden* on our own servers.

- Most CDNs have servers all over the globe so CDN's servers may be geographically nearer to your
users than your own servers. *Geographical distance* affects latency proportionally.

- CDNs are already configured with proper *cache settings*. Using a CDN saves further configuration
for static assets on your own servers.
