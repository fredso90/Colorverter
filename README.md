# Colorverter
Simple conversion between some of the most common color code formats. C# Class Library.

## License
MIT-license. Feel free to use this library as you wish.

## Installation
Make a reference to the Colorverter.dll file. In Visual Studio this can be done by navigating to Project -> References -> Add Reference.
Remember to add a using statement:
```
using Colorverter;
```

# How To Use Colorverter

All methods in Colorverter are tied to a class called "clrvrtr" which you will have to reference in order to use any of the methods. The naming convention I've used is FormatToFormat.
In cases where the format is an acronym, all letters in the format name is capitalized. In other cases only the first letter is capitalized. For example: RGBToHex.

## RGBToHex
The RGBToHex method takes an array of three(3) integers as an argument. These three integers represent the values red, green and blue in the RGB format.
It will then return the hexadecimal color code as a string.
```
int[] RGB = new int[] {255, 0, 0};
string testColor = clrvrtr.RGBToHex(RGB);
Console.WriteLine(testColor);
// Output would be: ff0000
```
