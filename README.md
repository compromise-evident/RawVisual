<!--
Complete raw analysis of any file.
-->



<p align="center">
  <img src="https://github.com/compromise-evident/ByteVisual/blob/main/Other/ByteVisual_icon.png" width="175">
</p>

<p align="center">
  <img src="https://github.com/compromise-evident/ByteVisual/blob/main/Other/App.png">
</p>

(ByteVisual.apk was made from ByteVisual.cpp and ByteVisual_icon.png using C4droid)

<p align="center">
  <img src="https://github.com/compromise-evident/ByteVisual/blob/main/Other/Terminal.png">
</p>

[Auditing in the browser?](https://coliru.stacked-crooked.com/a/14d9d24f1c3a8588)



**ByteVisual.cpp is my most-referenced file when building a tool, so should it be yours. So what can it do?**

Many things if you apply reasoning and logical deduction. Try creating a text file on Windows, paste it on pastebin.pl, and download the paste. You'll notice the files are different sizes (yes, ctrl+c will pick up \r\n as intended.) Now let ByteVisual take a look. You'll see that pastebin.pl had stripped away 1 Byte for every "enter" in the file. Try it and see which Byte it is, then read about them in ByteVisual.cpp. You'll learn about the \r\n fuckery of copy/paste, how to deal with each byte like an integer then revert, how to use Bash in C++, data types without unspecified behavior, how to properly use gparted, and how to tell if your files have hidden characters.

In the terminal sample above, characters 191 and 195 are contiguous in the file--producing 1 special character where if selected in Geany, stats show 2 selected items. The char is ÿ and to find this character in Geany, select text until you reach the Byte index (Shift + arrow keys.) The sample index of the 1st special character is 22,088.

```text
cout << char(195) << char(191);
```
prints only the one char ÿ to the terminal. It's 2 Bytes long, select, paste it, and check file size.
