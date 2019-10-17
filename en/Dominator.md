TOPIC: Dominator
AUTHORS: Teoli; teoli@mozilla.net; mdn:teoli
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy

# Dominator

In graph theory, node A dominates node B if every path from the root node to B passes through A.

This concept is important for garbage collection because it means that B is only reachable through A.
So if the garbage collector found A to be unreachable and eligible for reclaiming, than B would also
be unreachable and eligible for reclaiming. So objects that A dominates contribute to the retained
size of A: that is, the total amount of memory that could be freed if A itself were freed.

## Learn More

### General Knowledge

- [Dominator](https://en.wikipedia.org/wiki/Dominator%20(graph%20theory)) on Wikipedia

### Technical Reference

- [Dominators](https://developer.mozilla.org/en-US/docs/Tools/Memory/Dominators)
- [Memory Management](https://developer.mozilla.org/en-US/docs/Mozilla/js-ctypes/Using_js-ctypes/Memory_Management)
in JavaScript
- [Garbage Collection](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management#Garbage_collection)
