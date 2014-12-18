-# Part One

# Minimum Viable Unit Testing

Unit testing is not new. It has been around since the first computer programs were written. It may not always have been called Unit Testing, but the fundamentals have always been there. So what _is_ a Unit Test? We'll discuss that question in more depth in the next chapter, but for now this definition should suffice:

"A unit test is a piece of code that verifies an expectation about another piece of code - usually in the same language"

A simple example might be an `if` statement that checks a condition. If the condition is not met it takes some action, such as printing to the console, throwing an exception or terminating the process (or some combination thereof).

Sometimes these checks are conditionally compiled only in a testing build - which we will often refer to as a *debug* build.

In time this concept was wrapped up into concise functions or macros provided in the language or its associated libraries. Perhaps the most famous of these is C's `assert` macro.

In any C-family language the simplest example of a unit test is probably something like the following:

{title="Example 1: A complete C program with assert"}
~~~~~~~~
#include <assert.h>

int add( int a, int b ) {
  return a+b;
}

int main() {
  assert( add( 1,2 ) );
}
~~~~~~~~