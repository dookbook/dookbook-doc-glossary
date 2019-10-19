TOPIC: Type Conversion
AUTHORS: Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Jonathan Barrios; jonathan-barrios@mozilla.net; mdn:jonathan-barrios
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Ajinkya Patil; ajinkya_p@mozilla.net; mdn:ajinkya_p

# Type Conversion

Type conversion (or typecasting) means transfer of data from one data type to another.
Implicit conversion happens when the compiler automatically assigns data types, but the source code
can also explicitly require a conversion to take place. For example, given the instruction `5+2.0`,
the floating point `2.0` is implicitly typecasted into an integer, but given the instruction
`Number("0x11"`), the string "0x11" is explicitly typecasted as the number 17.
