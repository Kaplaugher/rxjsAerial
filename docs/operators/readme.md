# Operators

## combineLatest

Why Use combineLatest?

This operator is best used when you have multiple, long-lived observables that rely on eachother for some calculation or determination.
Be aware that combineLatest will not emit an initial value until each observable emits at least one value. This is the same behavior as withLatestFrom and can be a gotcha as there will be no output and no error but one (or more) of your inner observables is likely not functioning as intended, or a subscription is late.

![An image](../images/combineLatest.png)

In these examples, combine latest is being used to combine observables. The first being the user$ and sortSubject$. The second example combines the user$ and filterText.

## map

Why Use Map?

The Map operator applies a function of your choosing to each item emitted by the source Observable, and returns an Observable that emits the results of these function applications.  

![An image](../images/combineLatest.png)

In the first example, map is used to return the data of the observable. In the second example,

## pipe

As of RxJS 5.5 observables now have a pipe method available on the instances allowing you to clean up the code by calling pipe with all our pure functions operators. It is essentially chaining operators.

![An image](../images/combineLatest.png)

In the example, pipe is used to chain all the operators on the users$ observable.

## switchMap
