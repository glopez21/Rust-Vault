# Macros

`!` It specifies that the preceding name indicates a macro. Without such a symbol, print would instead indicate a function. There is no such function in the Rust standard library, and so you would get a compilation error. A macro is a thing similar to a function - it’s some Rust code to which a name is associated. By using this name, you ask to insert such code in this point.

## “literal string” phrase

The word “string” means “finite sequence of characters, possibly including spaces and punctuation”. The word “literal” means “with a value specified directly in source code.” Therefore a “literal string” is a “finite sequence of characters (possibly including spaces and punctuation) specified directly in source code”

# Command-Line Script

The `rustc` command shown above has a drawback: it prints all the errors it finds in your code in the order in which it finds them. Well, often your code will contain many syntax errors, and you should process them from the first one to the last one. But after the compiler has finished printing the errors, you are faced with the new prompt preceded by the last error found. So, you have to scroll back to the first error. A way to improve this situation is to use a command-line script, whose syntax depends on the operating system.

In a Linux system, you can put the following lines in a new script file:

`clear` 
`rustc $* --color always 2>&1 | more`

In a Windows system, you can put the following three lines in a .BAT file:

`@echo off` 
`cls` 
`rustc %* --color always 2>&1 | more`

If the script file is named, say, `rs (rs.bat on Windows)`, to compile a file named [main.rs](http://main.rs/) you can type:

`rs [main.rs](<http://main.rs/>)`

	This script first clears the screen, then runs the `rustc` compiler with all the arguments you give to it. If the compilation is successful, or if it generates less than a screenful of error messages, it behaves like a normal run of `rustc`.

	Otherwise, it fills the screen with error messages, and then stops, and shows the message --More-- at the bottom of the terminal screen. At this point you can press:

	• The Enter key, to advance by one line. 
	• The Space key, to advance by one screenful. 
	• The Q key (for “quit”), to abort printing error messages, and get back to the command prompt.

# Comments

```jsx
// This program
// prints a number.
print!("{}", 34); // thirty-four
/* print!("{}", 80);
*/
```

Rust programmers usually avoid the multi-line comment in production code, using only single line comments, and use multi-line comments only to exclude temporarily some code from compilation.

Rust comments look identical to modern C language comments. In fact, there is an important difference between Rust comments and C comments: Rust comments may be nested, and they must be nested correctly.