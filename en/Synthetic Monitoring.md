TOPIC: Synthetic Monitoring

# Synthetic Monitoring

**Synthetic monitoring** involves monitoring the performance of a page in a 'laboratory' environment,
typically with automation tooling in an environment that is as consistent as possible. With a
consistent baseline, synthetic monitoring is good for measuring the effects of code changes on
performance. However, it doesn't necessarily reflect what users are experiencing.

Synthetic Monitoring involves deploying scripts to simulate the path an end user might take through
a web application, reporting back the performance the simulator experiences. Examples of popular
synthetic monitoring tools include [WebPageTest](https://webpagetest.org/) and [Lighthouse](https://developers.google.com/web/tools/lighthouse/).
The traffic measured is
not of your actual users, but rather synthetically generated traffic collecting data on page performance.

Unlike RUM, synthetic monitoring provides a narrow view of performance that doesn't account
for user differences, making it useful in getting basic data about an application's performance and
spot-checking performance in development environments. Combined with other tools,
such as network throttling, can provide excellent insight into potential problem areas.

## See Also

- [Real User Monitoring (RUM)](https://wiki.developer.mozilla.org/en-US/docs/Glossary/Real_User_Monitoring)
- [Real User Monitoring (RUM) versus Synthetic Monitoring](https://wiki.developer.mozilla.org/en-US/docs/Web/Performance/Rum-vs-Synthetic)
- [Beacon](https://wiki.developer.mozilla.org/en-US/docs/Glossary/beacon)
