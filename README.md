Just a repo for me to try out some of the examples from the book "secrets of the Java Script Ninja", and record what I learnt

####[Function Declarations] (chapter3/functionDeclaration.html)####

This page demonstrates the different ways to declare functions. 

Including
* A named function that is available through a property of the window.
* An anonymous function that is a available through a property of the window. 
* An anonymous function that is available as a property of the window explicitly. 

It also demonstrates forware referencing, where by a function is in scope before it has been declared. And the difference between the function name and the window property it is available through.


####[Outer Inner Scope] (https://github.com/davidkethel/javaScriptNinja/blob/master/outerInnerScope.html) ####

Scope in javascript is not defined by braces but rather by function declarations, and that the global scope acts like on big function definition.

Named functions are in scope within the entire function in which they are declared. 

Variables are in scope after they have been decalred to the end of the function in which they are declared. 


#### [Apply Call] (https://github.com/davidkethel/javaScriptNinja/blob/master/applyCall.html) ####

It is possible in java script to invoke a function and give it any object we want as its context. 

There are 2 ways to do this

* Apply - Passed 2 parameters. The object to be used as the context, and an array of values to used as arguments to the function.
* Call - Multiple parameters. The first parameter is the object to be used as the context, then all the variables to be used as arguments to the function.


#### [Call Backs] (https://github.com/davidkethel/javaScriptNinja/blob/master/callbacks.html) ####

This page demonstrates a nifty use of the call function. 

It creates a for each function that takes an array and a function. The for each function calls the function for each element in the array, using the element 
as the context of the call. 

This also demonstrates a more "functional" way thinking witin java script. 

#### [Anonymous Function] (https://github.com/davidkethel/javaScriptNinja/blob/master/simpleAnonynousFunctions.html) ####

Demonstrates a couple of usages of the anonymous functions (Function defined without a name) including

* As an event handeler
* On a property of an object
* As the callback to the setTimeout function

#### [Function with 2 Names] (https://github.com/davidkethel/javaScriptNinja/blob/master/functionWithTwoNames.html) ####

This pretty cool example of a function that has its own name but is also referenced by a variable, so in a sense it has 2 names. 

Except that the function name is only available within the function. 


#### [Object/This] (https://github.com/davidkethel/javaScriptNinja/blob/master/objectThis.html) ####

Demonstrates the usage of of a function as an object constructor. Also shows that the This refers to individual objects context.

#### [Simple Recursion] (https://github.com/davidkethel/javaScriptNinja/blob/master/simpleRecursion.html) ####

This example demonstrates recusion by using a named function. 

#### [Recusion using an Object property] (https://github.com/davidkethel/javaScriptNinja/blob/master/simpleRecursion_WithObjectProperty.html) ####

This example is similar to the above example, except that the recursive function is now an anonymous function assigned to an object property. 

#### [Problem with above recursion] (https://github.com/davidkethel/javaScriptNinja/blob/master/simpleRecursion_WithObjectProperty_ObjectReset.html) ####

This example demonstrates a problem with the above example. The samurai object has reference to the say method on the Viking object. This is a problem because the say method calls itself by referencing the Viking object. 

So trying to run the samruai.say method after the Viking object has been reset causes an error as there is not viking.say to call in the recursive function.

#### [Solving function recursion problem] (https://github.com/davidkethel/javaScriptNinja/blob/master/simpleRecursion_WithFunctionName_ObjectReset.html) ####

To solve the above problem we can give the function a name, and call the functions name rather then the property refernce inside the function. 

This way it doesn't matter if the ninja object has been reset as the say function call it self by it own name. 
