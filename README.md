# MD-Parola-russian-font
<p align="right">
  <a href="./README.md">English</a>
  |
  <a href="./README-RU.md">Русский</a>
</p>

**Russian font for the MD_Parola library. Before compiling, you need to check the presence of the Parola_Fonts_data.h file in the `\Arduino\libraries\MD_Parola\src\` folder, if it is not there, you need to copy it from the`\Arduino\libraries\MD_Parola\examples\Parola_Fonts\` folder to `\Arduino\libraries\MD_Parola\src\`. Also check that the contacts and `HARDWARE_TYPE` are specified correctly.**

How does character encoding work: The first digit is the width of the character, followed by a number (their number is equal to the first digit). Each digit is in the decimal number system, when converted to binary we get lit LEDs. For example, I will take the letter A: `5, 124, 18, 17, 18, 124,    // 65 - 'A'`    (The number after `//` is the ASCII code of the character)

```
124⠀⠀18⠀⠀17⠀⠀18⠀⠀124
⠀↓⠀⠀⠀↓⠀⠀⠀↓⠀⠀⠀↓⠀⠀⠀↓
⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀⠀⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.
⠀0⠀⠀⠀1⠀⠀⠀0⠀⠀⠀1⠀⠀⠀0⠀⠀⠀⠀⠀⠀⠀.⠀⠀⠀█⠀⠀⠀.⠀⠀⠀█⠀⠀⠀.
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀⠀>⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀1⠀⠀⠀1⠀⠀⠀1⠀⠀⠀1⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀ █⠀⠀⠀█⠀⠀⠀█⠀⠀⠀█
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀⠀⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.
```

You can add any language knowing the `ASCII` encoding of its characters.

