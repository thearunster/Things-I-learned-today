# Guard clause

A guard clause is a chunk of code at the top of a function (or block) that serves a similar purpose to an assert or precondition. The idea is that when you have something to assert in the beginning of a method — do this using a fast return.

It typically does one (or any or all) of the following:
1. checks the passed-in parameters, and returns with an error if they're not suitable.
2. checks the state of the object, and bails out if the function call is inappropriate.
3. checks for trivial cases, and gets rid of them quickly.

For example ...
  ```c#
  draw() {
    if (!isVisible()) return;
    ...
  }
  ```
  
  ### Further reading
  
  * [http://wiki.c2.com/?GuardClause](http://wiki.c2.com/?GuardClause)
  * [Medium article on guard clause](https://medium.com/@scadge/if-statements-design-guard-clauses-might-be-all-you-need-67219a1a981a)
