# Unexpected Behavior When Directly Modifying Instance Variables in Ruby

This repository demonstrates a common, yet subtle, error in Ruby: directly manipulating instance variables using methods like `instance_variable_set` or `instance_variable_get`. While these methods offer flexibility, they can easily introduce bugs and make your code harder to maintain.

## The Problem

The example code showcases a simple class with a getter method.  Modifying the instance variable directly, bypassing the getter and setter, can break encapsulation and lead to unexpected behavior if other parts of the code rely on the getter or setter's logic.

## The Solution

Always use getter and setter methods to access and modify an object's internal state. This ensures that any validation or logic associated with these methods are correctly executed.