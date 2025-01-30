# Unexpected Behavior When Modifying Instance Variables Directly in Ruby

This repository demonstrates a common, yet easily overlooked, issue in Ruby: inconsistencies arising from directly manipulating instance variables without proper synchronization with accessor methods.  Directly modifying instance variables using `instance_variable_set` or `instance_variable_get` can lead to discrepancies between the perceived state of an object and its actual internal state.

The `bug.rb` file showcases the problem.  The `bugSolution.rb` file provides a corrected version that emphasizes the importance of using accessor methods for consistent and predictable behavior.

**Problem:**  The accessor method (`value`) in the initial example doesn't reflect changes made to the `@value` instance variable using `instance_variable_set`. This creates a mismatch between the reported value and the actual internal state. 

**Solution:** Always utilize accessor methods (getter and setter) to update and retrieve instance variables. This maintains consistency and enhances the maintainability and readability of the code.