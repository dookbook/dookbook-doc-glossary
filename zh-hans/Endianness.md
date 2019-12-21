TOPIC: Endianness

# Endianness

字节序，或字节顺序（"Endian"、"endianness" 或 "byte-order"），描述了计算机如何组织字节，组成对应的数字。

每个内存存储位置都有一个索引或地址。每一字节可以存储一个8比特(位)数字（即 介于`0x00` 和 `0xff` 之间），因此，你必须保留不止一个字节来储存一个更大的数字。现在，
大部分需占用多个字节的数字排序方式是 **little-endian**（可称小字节序、低字节序，即低位字节排放在内存的低地址端，高位字节排放在内存的高地址端。与之对应的big-endian
排列方式相反，可称大字节序、高字节序），所有的英特尔处理器都使用little-endian。little-endian的意思是使用低位储存更重要的信息，
least-to-most-significant（最低有效（least significant）字节取第一个位置，或者说，地址最低的位置），
可类比欧洲通用的日期书写方式（例如，31 December 2050。译者注：年份是最重要的，月份其次，日期最后）。

自然, **big-endian**是相反的顺序, 可类比ISO日期格式（例如：2050-12-31）。
big-endian 通常被称作"网络字节顺序"（"network byte order"）, 因为互联网标准通常要求数据使用big-endian存储，从标准Unix套接字（socket）层开始，
一直到标准化网络的二进制数据结构。此外，老式Mac计算机的68000系列和PowerPC微处理器曾使用 big-endian。

举个例子，用不同字节序存储数字`0x12345678`（即十进制中的`305 419 896`）：

- little-endian：`0x78 0x56 0x34 0x12`
- big-endian：`0x12 0x34 0x56 0x78`
- mixed-endian（文物，非常罕见）：`0x34 0x12 0x78 0x56`
