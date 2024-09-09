# Pengu Cheat Sheet

## Whitespace

Pengu is a whitespace-aware language. This means that instead of using [ ] or { } to delimit sections of code, we use line breaks and indentation.

This means that the way you indent your code is important. Fortunately, Pengu doesn't care how you do it, it just requires that you be consistent.

An indent must be at least 2 spaces or 1 tab, but you can use as many as you like. All code snippets on this page will use two spaces, in fact, the standard library will use only 2 spaces.

## Comments

Comments are just like Moonscript and Lua.

``` Lua
-- The longest comment in the world.
```

## Variables

Variables when assigned do not need to be given a type as the compiler can know it and give it to the variable. Strings and characters can use " or ' it doesn't matter.

``` Moonscript

simple_integer = 1

a_float = 1.0
other_float = 1f

same_with_doubles = 3d

character = "s"
my_string = 'Hola Mundo!'

i_can_fly = false

```

Also, just like in cpp you can assign multiple variables in a single line.

``` Moonscript

x, y, z = 1, 2, 3

```

You can create constants.

``` javascript 
const PI = 3.1416
```

If you only declare a variable to assign it later, then you must give it a type.

``` Python

index: int

index = 1

```

Another IMPORTANT rule is that variables can only be created inside a function for more security as in the V language.

## Functions

Functions are a weird mix between Moonscript and Typescript. Let's see it in the classic Cpp main function but now in Pengu.



``` Moonscript
main = (argc: int, argv: string): int -> 
  0
```

Oh, and the last statement will be returned if we gave a return type.

If we decide to make an empty function that does not return anything, we can declare the function more briefly.

``` Moonscript
short_function = ->
  hi!
```

Can I make functions with parameters with default values ​​like in Python? Yes, and in fact, if you do that you no longer need to give it a type.

Do you want to create an even shorter function and still use default values? No problem, if it's simple you can do it in one line.

``` Moonscript
simple_sum = (x = 10, y = 5): int -> x + y
```

## Function Calls

Unlike Moonscript, in Pengu function calls that require arguments must be enclosed in parentheses for easier reading, but if they do not require arguments, we simply use an exclamation mark.

``` Moonscript
sum(10, 20)
say_hi!
```