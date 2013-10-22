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

#### [5.2 Not So Simple Closure] (chapter5/5.2_NotSoSimpleClosure.html) ####

In this example we can see that the closure created by the declaration of innerFunction creates a closure that includes both innerValue and outerValue. innerFunction is able to access these variables even after their original scope has gone away, because they were in scope at the time the function was declared. 

#### [5.3 What eles closures can see] (chapter5/5.3_WhatElseClosuresCanSee.html) ####

A closure has access to the Function parameters, all variables in an outer scope even those declared after the function declaration.

#### [5.4 Private Variables With Closures] (chapter5/5.4_PrivateVariablesWithClosures.html) ####

This example demonstrates using closures to imitate private variables. The variable itself is declared within a function as is not accessible outside of it. However the access functions create closures that include the private variable.

#### [5.5 Closures in Ajax call Back] (chapter5/5.5_ClosuresInAjaxCallBack.html) ####

This example uses closures to enable access to the testSubject element in both the click and ajax success call back functions. 

#### [5.6 Closure in Animation] (chapter5/5.6_ClosureInAnimation.html) ####

Code within the setInterval callback can access the Tick, elem and the timer itself because of the closure. It also shows that because those variables are within the animateIt function, each time the function is called each closure gets a separate set of variables. Therefore you can animate multiple elements without their variable conflicting. 

#### [5.7 Binding A Specific Context to A Function] (chapter5/5.7_BindingSpecificContextToAFunction.html) ####

We can see in this example that the context for the click callback is not the object we expected but rather the element the the click was on. 

#### [5.8 Binding A Specific Context to A Function FIXED] (chapter5/5.8_BindingSpecificContextToAFunction_Fixed.html) ####

In order to fix the above problem by introducing a bind method. The anonymous function within the bind function creates a closure that includes the parameters of the bind function. This enables the button object to be the context of the click handler.

#### [5.10 Partially Applying arguments to a Native Function] (chapter5/5.10_PartiallyApplyingArgumentsToANativeFunction.html) ####

This is an example of partially applying a function. The native string split function has the regular expression that it uses prefilled. This then creates a new function that can be used to split a csv string.

#### [5.11 Curry Function] (chapter5/5.11_CurryFunction.html) ####

This is a simple example of simple partial function. It returns an anonymous function that includes the name of the function and any arguments in its closure. When called it calls the function applying the first argument to it.

#### [5.12 A more complex partial function] (chapter5/5.12_AMoreComplexPartialFunction.html) ####

This is a more complex version of the partial function above. It allows for multiple parameters to be prefilled. It does this by looping through all the arguments and placing them in the undefined holes of the parameter list.

#### [5.14 Self memoizing function using closures] (chapter5/5.14_SelfMemoizingFunctionUsingClosures.html) ####

This is another way of doing self memoizing function like from chapter4, this example uses closures. The memoize function return an anonymouse function that includes the function that is too memoized in its closure. When executes the anonymous function runs the memoized function with the original function as the context.

#### [5.15 Function Wrapping] (chapter5/5.15_FunctionWrapping.js) ####

An small function wrapping function. It allows for the original function implementation to wrapped in a new implementation.

#### [5.16 Enforcing the use of a name within an enclosed scope] (chapter5/5.15_EnforcingTheUseOfANameInAEnclosedScope.js) ####

This demonstrates the use of an imediatly executed function to enforce the use of a name with a function. Out side of the function "$" is not a reference to jQuery, however when the imediate function is executed the jquery object is passed in and bound to the "$" parrameter.