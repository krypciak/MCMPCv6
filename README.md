PROJECT ARCHIVED. THE NEWER VERSION CAN BE SEEN [HERE](https://github.com/krypciak/MCMPCv7).

DOCUMENTATION NOT FINISHED.

MCMulator PC v6 is an Integer based Minecraft computer.<br>

<h2>Screen</h2>
<ul>
  <li><strong>RGB</strong>
    <ul>
       <li>Max size: 240x240</li>
       <li>Colors: RGB, ~16 million colors</li>
    </ul>
  </li>
  <li><strong>16 color palette</strong>
    <ul>
      <li>Max size: 170x170 (Easly expandable)</li>
      <li>Colors:&nbsp;  white, yellow, orange, red, magenta, purple, blue, light blue, lime, green, brown,</li>
      cyan, light gray, pink, gray, black (Minecraft concrete colors)
    </ul>
   </li>
</ul>
<br>
<h2>Storage</h2>

In MCMPCv6, storage is based on <strong>NBT</strong>. Integers are stored in jukeboxes.<br>
Data is accessed by an NBT path:<ul> <li>For RAM and IDD: <em>RecordItem.tag.a</em></li><li>For PES: &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<em>RecordItem.tag.a[<strong>INDEX</strong>]</em></li></ul><br>
The position of the armor stand reading data is calculated with<br> this equation: &nbsp;&nbsp;x = cell % storageWidth,&nbsp; z = cell / storageWidth<br>

<h4>Types of storage</h4>
<ul>
  <li><strong>RAM</strong><ul>
      <li>Size: 250 (Easly expandable)</li>
      <li>1 dimensional</li>
      <li>Flushed at program start</li>
      <li>Fastest of all 3</li>
    </ul></li>
  <li><strong>PES (Program Execution Space)</strong><ul>
      <li>Size: 250X250 = 62500 (Easly expandable)</li>
      <li>2 dimensional</li>
      <li>Instead of a single integer, there's an 11-integer array.</li>
      <li>This storage is used for storing instructions, 1 instruction = 1 jukebox</li>
    </ul></li>
    <li><strong>IDD (Integer Data Drive)</strong><ul>
      <li>Size: 250X250 = 62500 (Easly expandable)</li>
      <li>2 dimensional</li>
      <li>This storage is used for storing data that isn't flushed on start,</li>it also supports 1 and 2-dimensional arrays
    </ul></li>
</ul>

<br>
<h2>CPU</h2>
The CPU uses <a href="https://github.com/krypciak/KLLL-Compiler-L1">KLLL Binary</a> for executing programs.<br>
You can write in <a href="https://github.com/krypciak/KLLL-Compiler-L1">KLLL L1</a> language or <a href="https://github.com/krypciak/KLLL-Compiler-L2">KLLL L2</a> languane.<br>
KLLL L2 is a higher-level language and it is converted to KLLL L1, so I recommend writing in KLLL L2.<br><br>
To see the instruction set click <a href="https://github.com/krypciak/KLLL-Compiler-L1/blob/main/README.md">here</a>.<br>

The speed of it depends on your IRL pc performance.<br>
For my PC, it's running at about 12500 IPS.<br>

To benchmark it, I used my fabric mod <a href="https://github.com/krypciak/MCFunction-Benchmark">MCFuntion Benchmark</a>

The optimized version is generated by a program I made called <a href="https://github.com/krypciak/MCMPCv6-Optimizer">MCMPCv6 Optimizer</a> and it is much faster than the raw version.<br>
However, you can't print logs with this version.<br>

