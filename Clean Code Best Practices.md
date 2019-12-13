### Functions
##### Functions should do one thing and one thing Importantly
It's hard to define what one thing is but the author of code complete said one thing can refer to one level of abstraction.

##### Error handling
1. Prefer try/catch to error codebase
2. Error handling is one thing, a function that has a try/catch should have nothing before or after the try/catch

##### Overloading
Consider using static factory methods when overloading a constructor.
Importantly use a function name that accurately describe the arguments.


`Complex fulcrumPoint = Complex.FromRealNumber(23.0)`

vs

`Complex fulcrumPoint = new Complex(23.0)`

##### Command Query Separation
Functions should do something or answer something, **but not both**. Either your function should set that state of an object or return some information on the object. Doing both leads to confusion.

Consider the following function:

`public boolean set(String attribute, String value)`

This functions sets the value of an object and returns true/false on success/failure

This can lead to a situation like:

`if (set('username', 'unclebob'))`

In this scenario what does this do? Does it:

1. Check if username was set to 'unclebob'
2. Check if username was set successfully to 'unclebob'

Renaming the function to `setAndCheckIfExists` is an alternative, however it doesn't help readability of the if statement. Ideally it should be something like:

```
if (attributeExists('username')) {
  setAttribute('username', 'unclebob')
}
```

### Comments
**Explain Yourself in Code**

Comments aren't always necessary, for example:

```
// Check to see if the employee is eligible for full benefits
if ((employee.flags & HOURLY_FLAG) && employee.age > 65)
```

vs

```
if (employee.isEligibleForFullBenefits())
```

### Tests
##### TDD Three Laws
1. You may not write production code until you have written a failing unit test
2. You may not write more of a unit test than is sufficient to fail, and not compiling is failing
3. You may not write more production code than is sufficient to pass the currently failing test

### Classes
##### Cohesion
Classes should have a small number of instance variables. Each of the methods of a class should manipulate one or more of those variables.

In general the more variables a method manipulates the more cohesive that method is to its class.

    A class in which each variable is used by each method is maximally cohesive.
