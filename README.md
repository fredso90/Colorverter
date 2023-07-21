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

All methods in Colorverter are tied to a class called "Clrvrtr" which you will have to reference in order to use any of the methods. The naming convention I've used is FormatToFormat.
In cases where the format is an acronym, all letters in the format name is capitalized. In other cases only the first letter is capitalized. For example: RGBToHex.

## RGBToHex
The RGBToHex method takes an array of three(3) integers as an argument. These three integers represent the values red, green and blue in the RGB format.
It will then return the hexadecimal color code as a string.
```
int[] RGB = new int[] {255, 0, 0};
string testColor = Clrvrtr.RGBToHex(RGB);
Console.WriteLine(testColor);
// Output would be: ff0000
```
## HexToRGB
The HexToRGB method takes a single string as an argument. Remember to not include "#" in the string. It will then return an array of three(3) integers.
```
int[] testColor = Clrvrtr.HexToRGB("ff0000");
foreach(int x in testColor)
{
  Console.WriteLine(x);
}
/* Output would be:
255
0
0
*/
```
## RGBToHSV
The RGBToHSV method takes an array of three(3) integers as an argument. These three integers represent the values red, green and blue in the RGB format.
It will then return an array of three(3) doubles representing the values Hue, Saturation, Value in HSV.
```
int[] testColor = new int[]{255, 0, 0};
double[] HSVColor = Clrvrtr.RGBToHSV(testColor);
foreach(double x in HSVColor)
{
  Console.WriteLine(x);
}
/* Output would be:
0
100
100
*/
```
## HSVToRGB
The HSVToRGB method takes an array of three(3) doubles as an argument. These doubles represent the values Hue, Saturation and Value in the HSV format.
It will then return an array of three(3) integers representing red, green and blue in the RGB format.
```
double[] HSVColor = new double[]{ 100, 0, 0 };
int[] RGBColor = Clrvrtr.HSVToRGB(HSVColor);
foreach(int x in RGBColor)
{
  Console.WriteLine(x);
}
/* Output would be:
255
0
0
*/
```
## HSVToHex
The HSVToRGB method takes an array of three(3) doubles as an argument. These doubles represent the values Hue, Saturation and Value in the HSV format.
It will then return a single string containing the hexadecimal color code.
```
double[] HSVColor = new double[]{ 100, 0, 0 };
Console.WriteLine(Clrvrtr.HSVToHex(HSVColor));
// Output would be: ff0000
```
## CMYKToRGB
The CMYKToRGB method takes an array of four(4) integers as an argument. These integers represent the Cyan, Magenta, Yellow and Black Key percent values in the CMYK format.
It will then return an array of three(3) integers representing the values for red, green and blue in the RGB format.
```
int[] CMYKColor = new int[] { 0, 100, 100, 0 };
int[] RGBColor = Clrvrtr.CMYKToRGB(CMYKColor);
foreach(int x in RGBColor)
{
  Console.WriteLine(x);
}
/* Output would be:
255
0
0
*/
```
## RGBToCMYK
The RGBToCMYK method takes an array of three(3) integers as an argument. These three integers represent the values red, green and blue in the RGB format.
It will then return an array of four(4) integers. These integers represent the Cyan, Magenta, Yellow and Black Key percent values in the CMYK format.
```
int[] RGBColor = new int[] { 255, 0, 0 };
int[] CMYKColor = Clrvrtr.RGBToCMYK(RGBColor);
foreach (int x in CMYKColor)
{
  Console.WriteLine(x);
}
/* Output would be:
0
100
100
0
*/
```
