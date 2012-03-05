---
layout: post
title: Reflection module
---

### ReflectionPackage ###

#### Methods ####

  * `getName()`: Returns a `String` containing the package name.
  {% highlight ruby %}
  ReflectionPackage pkg("std");
  println(pkg.getName("std)); // displays 'std'
  {% endhighlight %}

  * `getModules()`: Returns an `Array<String>` containing the packages' module.

  {% highlight ruby %}
  ReflectionPackage pkg("std");
  println(pkg.getModules()); // displays '[math, io, etc]'
  {% endhighlight %}

### ReflectionFunction ###

#### Methods ####

  * `isInternal()`: Returns a `Bool` indicating if the function is internal.

  * `isUserDefined()`: Returns a `Bool` indicating if the function is user-defined.

  * `getReturnType()`: Returns a `String` representing the name of return type.
  {% highlight ruby %}
  ReflectionFunction func("getcwd");
  println(pkg.getReturnType(); // displays 'String'
  {% endhighlight %}

  * `getNumRequiredArgs()`: Returns an `Int` representing the number of required arguments.
  {% highlight ruby %}
  ReflectionFunction func("max");
  println(pkg.getNumRequiredArgs(); // displays '2'
  {% endhighlight %}

  * `getArgs()`: Returns an `Array<String>` containing the type name of arguments.
