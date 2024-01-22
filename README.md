# How to code beautifully!
This file contains suggestions on how to write beautiful code, following some rules and habits that comes from the past and C origin.
This text is about C code, but maybe some of advices from here can be applied to other languages.

## Keyword/variable style
- Dont use camelCase <br>
- Snake_case is better option(```ip_opt,any_variable,ANY_CONSTANT,function_name()```)<br>
- truestyle is the best, but not always(```ipopt,anyvar,ANYCONST,funcname()```)<br>

## Size of var names
Try to make var names as simple and small as possible, if you can use name of var 
var1 var2 and the sense of the function code will remain clear, so do it without thinking.
It is okay to write big names for variables if this helps to make code clear and more understandable. The professional way to name return value is `res`.
<br>
<b>For example instead of:</b> <br>
```C++
unsigned int calculate_sum_of_two_integers(int first_value, int second_value)
{
    int result_of_the_sum;
    result_of_the_sum = first_value + second_value;
    return result_of_the_sum;
}
```
<b>Write this:</b>
```C++
uint32_t sum(int val1, int val2)
{
    int res;
    res = val1 + val2;
    return res;
}
```

## The brackets
Just look at the example <br>
```C++
int func(int val1, int val2)
{
    if(val1 < val2){
        return val1;
    }
    if(val1 > val2){
        return val2;
    }
    if(val1 == val2){
        return 0;
    }
}
```

## Infinit loops
Instead of `while(1)` use `for(;;)`

## Type names
do not use awfull big type names `unsigned int, unsigned char, unsigned long long`<br>
then use `<stdint.h>` -> `uint32_t,uint8_t,uint64_t`.<br>
Or even better way is to create your own types which looks like `u8,u16,u32,u64`.

## Functions beauty
Describe all variables in functions in the beggining of the function before using them and also create them in word size descending order(long string is placed higher), example:<br>
```C++
u32 func()
{
    u32 calc, res;
    u16 ipopt;
    u8 byte;
    ...
}
```

## Constants
Constants should be initialized in hex and written in capital case, and better way is to use `#define`
<br>
```C++
#define BYTE 0xA5
```

## General advices:

- Use `/* */` to comment instead of `//`
- Use assert it is important!!!!
- Dont use brackets if possible, for example in `if`
- To output var use `printf()`, for text use `puts()`, to skip line use `putchar('\n')`
- Do not be afraid to use `goto`, for example:<br> `ok: done: free: cleanup: out: retry: invalid: no: fail: bad: err:`
- instead of `const char* ch` write `const char *ch`
- if func isn`t in header file make it static
- huge strings should be line breaked, example: <br>
```C++
puts("kjhsdhfsdjklhfsdkljhf sdhjfg sdlkjhsdfkl \
 hsdkljf hgjkhdfkgjl hdkljgh dfkljgdfhgkljdfhgkl \
 jdfhgkldfjhgdflkj h");
```
- Write macros exactly where they are used
- If structer is used only in one function, create the structer inside it.
- Logicaly grouped variables can be created in one line `int dfs; int dfsa; int adfs` 
- For criticall exit use `panic()`
- write verbose() function
!> source https://youtu.be/r5z1rLZueTA?si=LSdtrqm1BxZlipIX
