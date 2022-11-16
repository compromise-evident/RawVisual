<!--
Byte occurrence print-out for any file, and C++/GNU+Linux resource in the cpp.
-->



<p align="center">
  <img src="https://github.com/compromise-evident/ByteResource/blob/main/Other/Terminal.png">
</p>

[Auditing in the browser?](https://coliru.stacked-crooked.com/a/ff6f9d44fd41f79c)



**ByteResource.cpp is my most-referenced file when building a tool, so should it be yours.**

### What can it do?

Many things if you apply reasoning and logical deduction. Try creating a text file on Windows, paste it on pastebin.pl, and download the paste. You'll notice the files are different sizes (yes, ctrl+c will pick up \r\n as intended.) Now let ByteResource take a look. You'll see that pastebin.pl had stripped away 1 Byte for every "enter" in the file. Try it and see which Byte it is, then read about them in ByteResource.cpp. You'll learn about the \r\n fuckery of copy/paste, how to deal with each byte like an integer then revert, how to use Bash in C++, data types without unspecified behavior, and how to properly use gparted. Enjoy the read.
