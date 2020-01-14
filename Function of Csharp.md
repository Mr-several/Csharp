# Learn to program

## string

1. print hello world

```c#
Console.WriteLine("Hello World!");
// consloe表示用于输出的控制台
// writeline表示在控制台上实现输出
```

2. Declare and use variables

```c#
string aFriend = "Bill";
Console.WriteLine(aFriend);
Console.WriteLine("Hello " + aFriend);
Console.WriteLine($"Hello {aFriend}");
// you can add a $ to declare the content between curly braces is a variable rather than a string.like format
Console.WriteLine($"The name {firstFriend} has {firstFriend.Length} letters.");
Console.WriteLine($"The name {secondFriend} has {secondFriend.Length} letters.");
// we can use length which is a property of a string
```

3. Trim string
string has a property trim, which can modify the leading spaces and the trailing spaces.

```c#
string greeting = "      Hello World!       ";
Console.WriteLine($"[{greeting}]");

string trimmedGreeting = greeting.TrimStart();
Console.WriteLine($"[{trimmedGreeting}]");

trimmedGreeting = greeting.TrimEnd();
Console.WriteLine($"[{trimmedGreeting}]");

trimmedGreeting = greeting.Trim();
Console.WriteLine($"[{trimmedGreeting}]");

>>>
[      Hello World!       ]
[Hello World!       ]
[      Hello World!]

```

4. replace string

```c#
string sayHello = "Hello World!";
Console.WriteLine(sayHello);
sayHello = sayHello.Replace("Hello", "Greetings");
Console.WriteLine(sayHello);
// Replace can replace first parameter using second paramter.
```

5. upper and lower

```c#
Console.WriteLine(sayHello.ToUpper());
Console.WriteLine(sayHello.ToLower());
>>>
GREETINGS WORLD!
greetings world!
```

6. judge an existance(contains)

```C#
string songLyrics = "You say goodbye, and I say hello";
Console.WriteLine(songLyrics.Contains("goodbye"));
Console.WriteLine(songLyrics.Contains("greetings"));
// contains return a bool value

string songLyrics = "You say goodbye, and I say hello";
Console.WriteLine(songLyrics.StartsWith("You"));
Console.WriteLine(songLyrics.EndsWith("hello"));
// to find the contain at the begining or the end of the string.
```

## integer and float

1. simple calculation

```c#
int a = 18;
int b = 6;
int c = a + b;
Console.WriteLine(c);
// remark: int c = a + b
```

2. precision and limits

```c#
int a = 7;
int b = 4;
int c = 3;
int d = (a + b) / c;
int e = (a + b) % c;
Console.WriteLine($"quotient: {d}");
Console.WriteLine($"remainder: {e}");
// 注意这种格式化的方法
```

3. double type

```c#
double a = 19;
double b = 23;
double c = 8;
double d = (a + b) / c;
Console.WriteLine(d);
// double is a type of float
```

4. decimal type
decimal has smaller range compared to double and integer, but has higher percision.

```c#
double a = 1.0;
double b = 3.0;
Console.WriteLine(a / b);

decimal c = 1.0M;
decimal d = 3.0M;
Console.WriteLine(c / d);
// remark M, this suffix indicate how to define a constant.
```

## conditional logic with branch and loop statements

1. if statement

```C#
int a = 5;
int b = 6;
if (a + b > 10)
    Console.WriteLine("The answer is greater than 10.");
// similar to matlab
```

2. if and else

```C#
int a = 5;
int b = 3;
if (a + b > 10)
    Console.WriteLine("The answer is greater than 10");
else
    Console.WriteLine("The answer is not greater than 10");
//not like python indentation is not significant when we have to write more than one statement we have to use curly braces.
if ((a + b + c > 10) && (a == b))
{
    Console.WriteLine("The answer is greater than 10");
    Console.WriteLine("And the first number is equal to the second");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
    Console.WriteLine("Or the first number is not equal to the second");
}
// remark: curly braces and && means "and" || means 'or'
```

3. while (like C) do while

* while

```c#
int counter = 0;
while (counter < 10)
{
  Console.WriteLine($"Hello World! The counter is {counter}");
  counter++;
}
```

* do while

when we use while it won't execute the code follwing while.
do while can execute the code following de firstly.

```c#
int counter = 0;
do
{
  Console.WriteLine($"Hello World! The counter is {counter}");
  counter++;
} while (counter < 10);
```

4. for loop

```c#
for(int counter = 0; counter < 10; counter++)
{
  Console.WriteLine($"Hello World! The counter is {counter}");
}
// like c, first condition means prime paramter, second condition means condition continues loop, third condition means the change of paramter after one loop.
```

5. combine for loop and if statement

```c#
int sum = 0;
for (int number = 1; number < 21; number++)
{
  if (number % 3 == 0)
  {
    sum = sum + number;
  }
}
Console.WriteLine($"The sum is {sum}");
```

## Array

1. creat a array

```c#
var names = new List<string> { "<name>", "Ana", "Felipe" };
// we specify the type of the element between the angle brackets.
foreach (var name in names)
// this is a loop for array?
// var? don't need to specify type of parament
{
  Console.WriteLine($"Hello {name.ToUpper()}!");
}
>>>
Hello <NAME>!
Hello ANA!
Hello FELIPE!
```

2. add and romove elements

```c#
Console.WriteLine();
names.Add("Maria");
names.Add("Bill");
names.Remove("Ana");
```

3. index of list

```C#
Console.WriteLine($"My name is {names[0]}.");
Console.WriteLine($"I've added {names[2]} and {names[3]} to the list.");
// use [] to specify the location of element in list.
```

C#不能使用超出范围的索引，只能使用小于count的索引，不能通过索引添加值。

4. property of list

* "count" which can figure out the number of element in list.
`Console.WriteLine($"The list has {names.Count} people in it");`

5. search and sort lists

```c#
var index = names.IndexOf("Felipe");
// indexof ourput the index of "felipe"
if (index != -1)
  Console.WriteLine($"The name {names[index]} is at index {index}");

var notFound = names.IndexOf("Not Found");
  Console.WriteLine($"When an item is not found, IndexOf returns {notFound}");
  // if output is -1 which means there isn't a specific element.
names.Sort();
// sort the elements in the list.
foreach (var name in names)
{
  Console.WriteLine($"Hello {name.ToUpper()}!");
}
  ```

6. a integer array

```c#
var fibonacciNumbers = new List<int> {1, 1};
// add your type between the angle brackets.
```


