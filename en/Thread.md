TOPIC: Thread
AUTHORS: Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09

# Thread

On modern computers and operating systems which are capable of running multiple tasks or programs at
the same time, each unit capable of executing code is called a **thread**. The **main thread** is
the one used by the browser to handle user events, render and paint the display, and to run the
majority of the code that comprises a typical web page or app. Because these things are all
happening in one thread, a slow web site or app script slows down the entire browser; worse,
if a site or app script enters an infinite loop, the entire browser will hang. This results in a
frustrating, sluggish (or worse) user experience.

However, modern JavaScript offers ways to create additional threads, each executing independently
while possibly communicating between one another. This is done using technologies such as web workers,
which can be used to spin off a sub-program which runs concurrently with the main thread in a thread
of its own. This allows slow, complex, or long-running tasks to be executed independently of the
main thread, preserving the overall performance of the site or app—as well as that of the browser
overall. This also allows you to take advantage of modern multi-core processors.

A special type of worker, called a service worker, can be created which can be left behind by a
site—with the user's permission—to run even when the user isn't currently using that site. This is
used to create sites capable of notifying the user when things happen while they're not actively
engaged with a site, such as notifying a user they have received new email even though they're not
currently logged into their mail service.
