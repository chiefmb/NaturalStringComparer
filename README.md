# NaturalStringComparer
[![Build status](https://ci.appveyor.com/api/projects/status/acwd0d2hwng5l5yh?svg=true)](https://ci.appveyor.com/project/chiefmb/naturalstringcomparer)

**Pure C# code**<br/>
**Usable in .net core and .net framework. No need to windows api.**<br/>
written int .net standard

Comparer to sort strings by numbers in them (as windows explorer do).<br/>
This is an easy to use and useful little library for programs that want to sort string naturaly by numbers.<br/>
you know 2 is lower than 11 but C# default string comparer not know this or not like this.<br/>
so you may like to use my lib for a human friendly string comparing and sorting.<br/>

```C#
var stringList = new List<string>
            {
                "number1", "number2", "number3", "number4", "number10", "number15", "number22", "number26"
                , "number9", "number33", "number5", "number12"
            };

stringList.Sort(NaturalStringComparer.Default);
//or
stringList.NaturalSort(); // need "using Gihan.Helpers.Linq;"

Console.WriteLine("Natural Sort:");
foreach(var item in stringList)
{
  Console.WriteLine(item);
}
stringList.Sort();
Console.WriteLine();
Console.WriteLine("Normal Sort:");
foreach(var item in stringList)
{
  Console.WriteLine(item);
}
/* output
Natural Sort:
number1
number2
number3
number4
number5
number9
number10
number12
number15
number22
number26
number33

Normal Sort:
number1
number10
number12
number15
number2
number22
number26
number3
number33
number4
number5
number9
*/
```
