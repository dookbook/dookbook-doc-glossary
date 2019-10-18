TOPIC: Perceived Performance
AUTHORS: Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Andy Stevens; andystevensname@github.com; github:andystevensname

# Perceived Performance

**Perceived performance** is a subjective measure of how fast a website seems to a user
based on load time and site responsiveness. This measure relies on human perception, not
an objective metric like time to interactive.

In terms of web performance, perceived performance is how fast a user interaction feels
rather than how fast an interaction actually is, be that a button press or a page load.
Perceived performance is not how fast your site is; it's how fast your users think it
is. Perceived performance is not measured by when your site is done loading but when it
has loaded enough for users to believe it has loaded and is interactive. In terms of
conversion rates, perceived performance is more important than the actual load and response times.

Speed Index is a common metric for measuring perceived performance, though it's
not perfect. Other features, such as good UX design, including animations, and lazy loading,
can make your site appear more responsive, even if the download and response times remain the same.

Actual performance is a measurement from when a request is made, through the downloading
parsing and execution of all resources, and the final paint. While increased performance
generally increases perceived performance, there are some techniques that can be used to
increase perceived performance while marginally decreasing actual performance.

There are front end optimization techniques that can improve perceived performance, such
as adding the `defer` or `async` attribute to scripts, or placing scripts at the end of
documents, and placing CSS in the head of documents.
