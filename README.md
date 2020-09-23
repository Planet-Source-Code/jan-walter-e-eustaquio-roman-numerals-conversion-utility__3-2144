<div align="center">

## Roman Numerals \- Conversion Utility\!


</div>

### Description

Well, this is i folks. This is the most ACCURATE and MODERN conversion from Arabic to Roman numerals... I use the strick rule of using roman numerals, based on the old and accurate use of it. Dont' know what is 1696 or 1999 on roman numerals? Then check this out!
 
### More Info
 
This is a good converstion utility from Arabic to Roman... If you forgot how to represent arabic numerals to roman forms, then try this and LEARN, the easy way! Thanks.

This code illustrates the use of strings, which is an array of characters. Illustrates how to use string copy, strcpy() from the STRING.H and good for beginners. Hope you like it!


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jan Walter E\. Eustaquio](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jan-walter-e-eustaquio.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |C\+\+ \(general\), Borland C\+\+
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__3-26.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jan-walter-e-eustaquio-roman-numerals-conversion-utility__3-2144/archive/master.zip)





### Source Code

```
//ROMAN.CPP - Converts Arabic to Roman numerals
// Inspired by 'The Never Ending Debate About Roman Numerals'
// Author: J@w3s
// Version: 1.1.6
// Modified: July 23, 2001
/********************************************************************
Well, here it is folks... the ACCURATE and MODERN CONVERSION
from ARABIC numerals to ROMAN numerals! Yes, and this is based
on the strick rule that every digit (thousands, hundreds, tens, ones)
represents an equivalent ROMAN digit.
Here is a quick review of the ROMAN NUMERALS:
I = 1	V = 5	X = 10	L = 50  C = 100
D = 500	M = 1000
So combining these values, we can represent numbers up to
thousands digits. This SOURCE CODE will compute for conversions
up to 3999. I will make more additions to support up to
millions digits (later ;)
An alternative way of depicting larger numbers is by putting
a horizontal bar over the numeral which multiplies it by 1000.
Say you put a horizontal bar over V, it becomes 5000, or over
X, it becomes 10,000.
On a larger scale 3,852,429 can be depicted as
MMMDCCCL MMCDXXIX
On a small scale like the value 1999 (which have many
versions of roman numerals, and most debates on how to
represent it) is
MCMXCIX
I hope you find this very useful. And pls vote for my code!
Thanks! This is dedicated to all of c++ programmers, and
roman numeral fanatics. ;)
***************************************************************/
#include<iostream.h>
#include<conio.h>
#include<string.h>
main()
{
char thou[4], huns[5], tens[5], ones[5];
int n, thd, hd, tnd, od;
clrscr();
cout << "\n -=[ ROMAN NUMERALS ]=-";
cout << "\n Enter a number (1 - 3999): ";
cin >> n;
thd = n / 1000;
hd = (n % 1000) / 100;
tnd =((n % 1000) % 100) / 10;
od = ((n % 1000) % 100) % 10;
switch(thd)
	{
	case 1: strcpy(thou, "M");
		  break;
	case 2: strcpy(thou, "MM");
		  break;
	case 3: strcpy(thou, "MMM");
		  break;
	default: strcpy(thou, "");
	}
switch(hd)
	{
	case 1: strcpy(huns, "C");
		  break;
	case 2: strcpy(huns, "CC");
		  break;
	case 3: strcpy(huns, "CCC");
		  break;
	case 4: strcpy(huns, "CD");
		  break;
	case 5: strcpy(huns, "D");
		  break;
	case 6: strcpy(huns, "DC");
		  break;
	case 7: strcpy(huns, "DCC");
		  break;
	case 8: strcpy(huns, "DCCC");
		  break;
	case 9: strcpy(huns, "CM");
		  break;
	default: strcpy(huns, "");
	}
switch(tnd)
	{
	case 1: strcpy(tens, "X");
		  break;
	case 2: strcpy(tens, "XX");
		  break;
	case 3: strcpy(tens, "XXX");
		  break;
	case 4: strcpy(tens, "XL");
		  break;
	case 5: strcpy(tens, "L");
		  break;
	case 6: strcpy(tens, "LX");
		  break;
	case 7: strcpy(tens, "LXX");
		  break;
	case 8: strcpy(tens, "LXXX");
		  break;
	case 9: strcpy(tens, "XC");
		  break;
	default: strcpy(tens, "");
	}
switch(od)
	{
	case 1: strcpy(ones, "I");
		  break;
	case 2: strcpy(ones, "II");
		  break;
	case 3: strcpy(ones, "III");
		  break;
	case 4: strcpy(ones, "IV");
		  break;
	case 5: strcpy(ones, "V");
		  break;
	case 6: strcpy(ones, "VI");
		  break;
	case 7: strcpy(ones, "VII");
		  break;
	case 8: strcpy(ones, "VIII");
		  break;
	case 9: strcpy(ones, "IX");
		  break;
	default: strcpy(ones, "");
	}
cout << "\n The equivalent roman numeral is: ";
cout << thou << huns << tens << ones;
getch();
return 0;
}
```

