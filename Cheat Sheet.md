Line Comments 

	// This is a line comment. 
	
Multi Line Comments 

	/* This is a multi line comment. 
		We can write multiple lines within this space. 
	*/ 
	
Doc Comments 
	
	/// This is used mainly to document functionality of things. 
	//! This is used mainly to document the content of crates. 
	
Markdown 
	
	Heading 
		//! # This is used to create a heading within a markdown comment. 
		//! ``` 
		//! In here we can comment methods functionalities for markdown documentation. 
		//!```

Directives

	#[allow(unused_variables)] --> Turns off the compiler warning about unused variables. 
	
	#[allow(unused_assignmnets)] --> Turns off the compiler warning about unused assignments. 
	
	#![allow(unused)] --> Turns off all compiler warning about unused stuff.


Style
_Let’s define and use a style throughout all scripts… for consistency._
_All programs must follow the style!_

	Directives 
	crates/libraries import 
	Script documentation 
	main function 
	
	#![alllow(unused)] 
	use crate::mod::method 
	
	/// Script/Crate Description 
	/// what is the crate/script about 
	
	fn main(){ 
	//! # Main Function Name 
	//! ``` 
	//! fn main() Description 
	//! ``` 
	//! Function description 
	
	// print this on every script yut yut 
	println!("Cheers! \u{1F37b}"); }

Functions

	Syntax: 
	
	fn function_name(args) { 
		//! # Function-Name Function 
		//! ``` 
		//! fn function_name(name: & mut &str) 
		//! ``` 
		//! Function description including the arguments description and return expected.. 
		...funtionality... 
	}


Closures

	// A Function within a function. 
	// Also known as anonymous function or lambda expressions. 
	// Sample Syntax 
	
		|a: i32, b: i32| println!("{}", a + b); 
			// If you have just one expression to calculate or evaluate, then this line should suffice. 
			
		|a: i32, b: i32| -> {a + b}; 
			// If you have a return type or multiple expression to evaluate, use this line. 
			
	// Closure can be assigned to a variable 
	
			let sum = |a: i32, b: i32| -> i32 {a + b}; sum(2, 3) 
			
	// Closures can be generic; which means that we do not have to declare their type explicitly 
	
			let gen = |x| { prinln!("received {}", x) }; 
			gen(3); 
			
	/* 
		Take notice: When using a generic enclosure expression; if that function is 
		made with an integer and later on we want to utilize the expression to 
		evaluate or calculate another data type, the rRust compiler will throw an 
		error. This is because Rust will designate that data type to that expression
		to provide memory safety throughout the script. Therefore, if we want to 
		use that expression with another data type, we must either re-initialise 
		the first expression call with a new assignment or create a new genetic 
		enclosure. 
	*/