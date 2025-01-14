# Overview

This repository is a part of the Java language training plan. Please read the following guidelines before start.

# Getting Start

## Basic Principals

Each repository contains a gradle java project with a number of unit tests. The initial state of all unit tests are *FAILED*. So the aim is to correct the failed test. Please follow the following steps to get the best experience:

* Read the test code and try to understand what it says.
* Trying to fix the test **WITHOUT RUNNING**. This is very important. Because once you run the test, you may find the failure message of the test telling you the expected result. That means you may lose the chance to figure it out by yourself. Note that you should **ONLY** be able to modify code within the **TODO AREA**. The code outside the **TODO AREA** is **NOT** changable.
* Run the test to examine if the fix is correct.
* Answer the following 4 questions after the test is passed.

The 4 questions are:

1. What is the knowledge point of the test? Where is the offical document to the knowledge point?
1. Why the test failed at first?
1. Why you corrected the test that way?
1. Do you have further questions on this knowledge point?

## Example

Let's take a look at an example:

```java
@Test
void should_pass_by_value() {
  int value = 5;

  tryingToUpdateValue(value);

  // TODO: please modify the following code to pass the test
  // <--start
  final int expected = 0;
  // --end-->

  assertEquals(expected, value);
}
```

First, read the test. From the title and code we can know that the test what to examine the behavior when passing an argument. We are not sure what `tryingToUpdateValue` does, so we can jump into its implementation:

```java
private static void tryingToUpdateValue(int value) {
  value += 2;
}
```

Now we have got the full context of the test. The argument is passed by value so the integer will be copied when passing into `tryingToUpdateValue`. Thus the value from the caller site will not change.

Notice that the todo area is in the test method. So we can modify codes within the todo area to pass the test:

```java
  // TODO: please modify the following code to pass the test
  // <--start
  final int expected = 5;
  // --end-->
```

Please note that not all todo areas are located in test method. And some todo area may have further restrictions, for example:

```java
  // TODO: You should not write concrete number here. Please find a property or constant instead.
  // <!--start
  final int maximumSymbol = 0;
  final int minimumSymbol = 0;
  // --end-->
```

The hint indicates that we should not write concrete number here. So I should not write `3` or `0xffffffff`, but write symbol (e.g. `Integer.MAX_VALUE`).

## Running Test

You could run unit tests with the help of IntelliJ. But it is also possible to run unit test via command line: `./gradlew build`.

If you just want to build your code without running test. Please use `./gradlew build -x test
`

should_perform_logical_boolean_operations:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- To be familiarized in checking boolean statements
2.Why the test failed at first?
- Misunderstood the way of checking inside actualResults array.
3.Why you corrected the test that way?
- Because I thought that it would output the values of actualResults
4.Do you have further questions on this knowledge point?
- None

should_do_bitwise_and_boolean_operation:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- To practice with bollean and binary codes
2.Why the test failed at first?
- I didn't know how to convert hexadecimals codes to binary
3.Why you corrected the test that way?
- Because that is the result of the binary when AND
4.Do you have further questions on this knowledge point?
- None

should_do_bitwise_or_boolean_operation:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- To practice with bollean and binary codes
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- Because that is the result of the binary when inclusive OR
4.Do you have further questions on this knowledge point?
- None


should_describe_escaped_chars:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- To practice escape characters
- https://www.freeformatter.com/java-dotnet-escape.html
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- Because that is the proper way or the escape format to prevent compilation errors
4.Do you have further questions on this knowledge point?
- None


should_describe_escaped_chars:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- To practice escape characters
- https://www.freeformatter.com/java-dotnet-escape.html
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- Because that is the proper way or the escape format to prevent compilation errors
4.Do you have further questions on this knowledge point?
- None

should_get_range_of_primitive_short_type:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- https://www.dotnetperls.com/integer-java
- Examine the MIN_VALUE and MAX_VALUE final ints on Short and other classes. Use loop boundaries.
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- This is the way to check the minimum value and maximum value of Short without using concrete numbers
4.Do you have further questions on this knowledge point?
- None

should_get_range_of_primitive_long_type:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- https://www.dotnetperls.com/integer-java
- Examine the MIN_VALUE and MAX_VALUE final ints on Long and other classes. Use loop boundaries.
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- This is the way to check the minimum value and maximum value of Long without using concrete numbers
4.Do you have further questions on this knowledge point?
- None

should_get_range_of_primitive_byte_type:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- https://www.dotnetperls.com/integer-java
- Examine the MIN_VALUE and MAX_VALUE final ints on Byte and other classes. Use loop boundaries.
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- This is the way to check the minimum value and maximum value of Byte without using concrete numbers
4.Do you have further questions on this knowledge point?
- None

should_overflow_silently:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- https://www.tutorialspoint.com/Java-overflow-and-underflow
- Examine the VALUE of Integer.MAX and what will happen if you overflow it
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- If you add 1 to the Integer.MAX it will overflow
4.Do you have further questions on this knowledge point?
- None

should_underflow_silently:
1.What is the knowledge point of the test? Where is the official document to the knowledge point?
- https://www.tutorialspoint.com/Java-overflow-and-underflow
- Examine the VALUE of Integer.MIN_VALUE and what will happen if you overflow it
2.Why the test failed at first?
- no failed test
3.Why you corrected the test that way?
- If you minus 1 to the Integer.MIN_VALUE it will overflow
4.Do you have further questions on this knowledge point?
- None


