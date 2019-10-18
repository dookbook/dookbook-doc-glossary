TOPIC: Guard
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone

# Guard

Guard is a feature of `Headers` objects (as defined in the Fetch spec, which affects
whether methods such as `set()` and `append()` can change the header's contents.
For example, immutable guard means that headers can't be changed.
For more `information`, read Fetch basic concepts: guard.
