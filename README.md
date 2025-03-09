# MD-Parola-russian-font
<p align="right">
  <a href="./README.en-US.md">English</a>
  |
  <a href="./README.md">Русский</a>
</p>
**Russian font for the MD_Parola library. Before compiling, you need to check the presence of the Parola_Fonts_data.h file in the `\Arduino\libraries\MD_Parola\src\` folder, if it is not there, you need to copy it from the`\Arduino\libraries\MD_Parola\examples\Parola_Fonts\` folder to `\Arduino\libraries\MD_Parola\src\`. Also check that the contacts and `HARDWARE_TYPE` are specified correctly.**

**Русский шрифт для библиотеки MD_Parola. Перед компиляцией необходимо проверить наличие файла Parola_Fonts_data.h в папке `\Arduino\libraries\MD_Parola\src\`, если его там нет, необходимо скопировать его из папки `\Arduino\libraries\MD_Parola\examples\Parola_Fonts\` в `\Arduino\libraries\MD_Parola\src\`. Также проверьте правильность указания контактов и `HARDWARE_TYPE`.**

How does character encoding work: The first digit is the width of the character, followed by a number (their number is equal to the first digit). Each digit is in the decimal number system, when converted to binary we get lit LEDs. For example, I will take the letter A: `5, 124, 18, 17, 18, 124,    // 65 - 'A'`    (The number after `//` is the ASCII code of the character)

Как работает кодировка символов: Первая цифра — ширина символа, за ней следует число (их количество, равно первой цифре). Каждая цифра идет в десятичной системе счисления, при переносе в двоичную получаем горящие светодиоды. Для примера возьму букву А: `5, 124, 18, 17, 18, 124,    // 65 - 'A'`  (Число после `//` — это ASCII-код символа)

```
124⠀⠀18⠀⠀17⠀⠀18⠀⠀124
⠀↓⠀⠀⠀↓⠀⠀⠀↓⠀⠀⠀↓⠀⠀⠀↓
⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀⠀⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.
⠀0⠀⠀⠀1⠀⠀⠀0⠀⠀⠀1⠀⠀⠀0⠀⠀⠀⠀⠀⠀⠀.⠀⠀⠀█⠀⠀⠀.⠀⠀⠀█⠀⠀⠀.
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀>⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀1⠀⠀⠀1⠀⠀⠀1⠀⠀⠀1⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀ █⠀⠀⠀█⠀⠀⠀█⠀⠀⠀█
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀1⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀1⠀⠀⠀⠀⠀⠀⠀█⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀█
⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀0⠀⠀⠀⠀⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.⠀⠀⠀.
```

You can add any language knowing the `ASCII` encoding of its characters.

Вы можете добавить любой язык, зная `ASCII` кодировку его символов.
