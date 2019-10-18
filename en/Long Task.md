TOPIC: Long Task

# Long Task

A **long task**  is a task that takes more than 50ms to complete. It is an uninterrupted period
where the main UI thread is busy for 50 ms or longer. Common examples include long running
event handlers, expensive reflows and other re-renders, and work the browser does between
different turns of the event loop that exceeds 50 ms.

## See Also

- [Long Task API](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Long_Tasks_API)
