TOPIC: Page Load Time
AUTHORS: Andy Stevens; andystevensname@github.com; github:andystevensname

# Page Load Time

**Page load time** is the time it takes for a page to load, measured from navigation start
to the start of the load event.

```javascript
let time = performance.timing;

let pageloadtime = time.loadEventStart - time.navigationStart;
```

While page load time 'sounds' like the perfect web performance metric, it isn't. Load times can
vary greatly between users depending on device capabilities, network conditions, and, to a lesser
extent, distance from the server. The development environment, where page load time is measured,
is likely an optimal experience, not reflective of your users' reality. In addition, web performance
isn't just about when the load event happens. It's also about perceived performance,
responsiveness, jank and jitter.

## See Also

- [Navigation and resource timing](https://wiki.developer.mozilla.org/en-US/docs/Web/Performance/Navigation_and_resource_timings)
- [`PerformanceNavigationTiming`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/PerformanceNavigationTiming)
- [`PerformanceResourceTiming`](https://wiki.developer.mozilla.org/en-US/docs/Web/API/PerformanceResourceTiming)
