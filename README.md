Just a repo for me to try out some of the examples from the book "secrets of the Java Script Ninja", and record what I learnt

####[3.1 Function Declarations] (chapter3/3.1_FunctionDeclaration.html)####

This page demonstrates the different ways to declare functions. 

Including
* A named function that is available through a property of the window.
* An anonymous function that is a available through a property of the window. 
* An anonymous function that is available as a property of the window explicitly. 

It also demonstrates forward referencing, where by a function is in scope before it has been declared. And the difference between the function name and the window property it is available through.


####[3.2 Outer Inner Scope] (chapter3/3.2_ScopingBehaviourOfDeclarations.html) ####

Scope in javascript is not defined by braces but rather by function declarations, and that the global scope acts like on big function definition.

Named functions are in scope within the entire function in which they are declared. 

Variables are in scope after they have been decalred to the end of the function in which they are declared. 


####[3.3 Function vs Method Invocations] (chapter3/3.3_FunctionVsMethodInvocation.html) ####

This page shows the difference between a function and method invocation of a function. The difference being the context that the function runs in. 

When invoked as function the context is the window. When invoked as a method the context is the object, 


#### [3.4 Using a Constructor to set common Objects] (chapter3/3.4_UsingAConstructorToSetUpCommonObjects.html) ####

Demonstrates the usage of of a function as an object constructor. Also shows that the This refers to individual objects context.

When a functions is used as a constructor. 
* A new object is created. 
* This object is passed to the constructor as "this".
* In The absence of any explicit return value, the new object is returned.


#### [3.5 Using the apply() and call() methods to supply the function context] (chapter3/3.5_UsingApplyCallMethodsToSupplyTheFunctionContext.html) ####

It is possible in java script to invoke a function and give it any object we want as its context. 

There are 2 ways to do this

* Apply - Passed 2 parameters. The object to be used as the context, and an array of values to used as arguments to the function.
* Call - Multiple parameters. The first parameter is the object to be used as the context, then all the variables to be used as arguments to the function.


#### [3.6 Building a foreach function to demonstrate setting a function context] (chapter3/3.6_BuildingForEachToDemonstrateSettingAFunctionContext.html) ####

This page demonstrates a nifty use of the call function. 

It creates a for each function that takes an array and a function. The for each function calls the function for each element in the array, using the element 
as the context of the call. 

This also demonstrates a more "functional" way thinking witin java script. 

#### [4.1 Common Examples Of Anonymous Functions] (chapter4/4.1_CommonExamplesOfAnonymousFunctions.html) ####

Demonstrates a couple of usages of the anonymous functions (Function defined without a name) including

* As an event handeler
* On a property of an object
* As the callback to the setTimeout function

#### [4.2 Recursion Using A Named Function] (chapter4/4.2_RecursionUsingANamedFunction.html) ####

This example demonstrates recusion by using a named function. 

#### [4.3 Recursion Using An Objects Property] (chapter4/4.3_RecursionUsingAnObjectsProperty.html) ####

This example is similar to the above example, except that the recursive function is now an anonymous function assigned to an object property. 

#### [4.4 Recursion Using An Objects Property Problem] (chapter4/4.4_RecursionUsingAnObjectsPropertyProblem.html) ####

This example demonstrates a problem with the above example. The samurai object has reference to the say method on the Viking object. This is a problem because the say method calls itself by referencing the Viking object. 

So trying to run the samruai.say method after the Viking object has been reset causes an error as there is not viking.say to call in the recursive function.

#### [4.5 Recursion Using An Objects Property Problem Fixed] (chapter4/4.5_RecursionUsingAnObjectsPropertyProblemFixed.html) ####

To solve the above problem we can give the function a name, and call the functions name rather then the property refernce inside the function. 

This way it doesn't matter if the ninja object has been reset as the say function call it self by it own name. 


#### [4.6 Function With Two Names] (chapter4/4.6_FunctionWithTwoNames.html) ####

This pretty cool example of a function that has its own name but is also referenced by a variable, so in a sense it has 2 names. 

Except that the function name is only available within the function. 

#### [4.7 Recursion Using Arguments Callee] (chapter4/4.7_RecursionUsingArgumentsCallee.html) ####

This example follows on from the other recursion examples, but it different in that its uses the arguments.callee property when the function calls its self. 

This is a far more reliable way of accessing the currently executing function.

#### [4.8 Storing a Collection of Unique Functions] (chapter4/4.8_StoringCollectionOfUniqueFunctions.html) ####

This example solves the problem of storing a unique collection of functions. When a function is added to the collection, the function gets an Id property. This way if there is an attempt to add the same function again, we can just look for the Id property to see if it’s been added.

#### [4.9 Memoizing Previously Computed Values] (chapter4/4.9_MemoizingPreviouslyComputedValues.html) ####

This example demonstrates another use of the function properties. Function properties can be used to store the value from previous executions of the function. That way minimizing any expensive computation.

#### [4.10 Simulating array like methods] (chapter4/4.10_SimulatingArrayLikeMethods.html) ####

This is a particularly interesting example in that demonstrates that you can call the array add function on an object that is not an array. It actually adds the element and increments the length property on the object. 

#### [4.11 Min and Max functions that work on arrays] (chapter4/4.11_MinMaxForArrarys.html) ####

This shows a cool way of calling the min and max function on an array. The Math.min and Math.max don't take arrays, put rather a varialbe lenght arrgument list. However you can use the Apply method to call them with an array. 

#### [4.12 Method Overloading With Variable Length Argument Lists] (chapter4/4.12_MethodOverloadingWithVariableLengthArgumentLists.html) ####

We can use the arguments parameter to simulating function overloading. 

#### [4.13 slicing the Argument list] (chapter4/4.13_SlicingTheArgumentList.html) ####

Another example of using the arguments parameter, however in this case, because the arguments parameter is an Array-Like and not an actual array we need to use “call” to make the slice method work on it.

#### [4.15 Add Method] (chapter4/4.15_AddMethod.js) ####

This is a little Java script function that adds a function to an object. It also allows for the adding of overloaded functions to object. It does this by first storing the previous function of the same name; it then invokes the new function if the number of parameters matches the number of arguments. If they don’t match then call the old function that has been stored. 

#### [4.16 Adding Variable Lenght Functions To An Object] (chapter4/4.16_AddingVariableLenghtFunctionsToAnObject.html) ####

Demonstrates the useage of the addMethod.

#### [5.1 A simple closure] (chapter5/5.1_SimpleClosure.html) ####

This is just a simple example of a closure where code with the outerFunction can access outerValue.


#### [5.2 Not So Simple Closure] (chapter5/5.2_NotSoSimpleClosure) ####

In this example we can see that the closure created by the declaration of innerFunction creates a closure that includes both innerValue and outerValue. innerFunction is able to access these variables even after their original scope has gone away, because they were in scope at the time the function was declared. 