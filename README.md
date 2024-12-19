# Unintended Read-Only Behavior with Getter Methods in Ruby

This repository demonstrates a subtle bug in Ruby related to the unintended read-only behavior of getter methods when not explicitly designed to allow modification.  The `bug.rb` file shows the problem, and `bugSolution.rb` illustrates how to resolve it.

**Bug:**  The `MyClass` attempts to modify the `@value` instance variable through the `value` method, however this will not change the internal state of the object. This is because the getter method doesn't have setter functionality.