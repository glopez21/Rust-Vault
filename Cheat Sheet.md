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
