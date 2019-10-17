TOPIC: Compile
AUTHORS: Julia Buchner; PetiPandaRou@mozilla.net; mdn:PetiPandaRou
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone

# Compile

Compiling is the process of transforming a computer program written in a given language into an
equivalent program of another language. A compiler is a software to execute this task. Sometimes,
this task is also referred to as "assembling" or "build", which typically indiciates more than just
compilation is done, e.g. packaging it in a binary format.

Usually, a compiler transforms a higher-level language such as C or Java, which humans understand,
into a machine language, such as assembly, that the CPU can understand. Some compilers which translate
between similar level languages are called transpilers or cross-compilers, for instance to compile
from TypeScript to JavaScript. Those are considered productivity tools.

Most Compilers work either ahead-of-time (AOT) or just-in-time (JIT). As a programmer, you usually
invoke AOT compilers from a command line or your IDE. The most famous, "gcc" is one example.
JIT compilers are usually transparent to you, used for performance. For instance in the browser:
Firefox' SpiderMonkey JavaScript Engine has a JIT built-in that will compile JavaScript
in a website to machine code while you're viewing it so it runs faster.
Projects like WebAssembly work on making this even better.

## Learn More

### General Knowledge

- [Compiler](https://en.wikipedia.org/wiki/Compiler) on Wikipedia
- The [GNU Compiler Collection (GCC)](https://gcc.gnu.org/)

### Learning Resources

- [Base CS Introduction on Compilers](https://medium.com/basecs/a-deeper-inspection-into-compilation-and-interpretation-d98952ebc842)
- [A big list of learning material on StackOverflow](http://stackoverflow.com/a/1672/133203)
