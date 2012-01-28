---
layout: post
---

#### Installing ####

To install **Clever** is easy, just run the `make`. In this stage, you can help
the *Clever Team* also by running `make run-tests` and reporting to us if you get
some failures!


#### Native data type

{% highlight ruby %}
Int i = 10;
Double j = 1.2;
String str = "foo";
Bool is = true;
Array<Int> arr;
Map<Int, String> map;
{% endhighlight %}

Native data types in Clever are *first-class object*. This means that you can do:

{% highlight ruby %}
"hello world!".toUpper()
{% endhighlight %}


##### const qualifier #####

You can mark a variable to not be changed along your code. Just use the `const`
qualifier.

{% highlight ruby %}
const Int i = 10;
{% endhighlight %}

#### Standards package

The standards (std) package counts with the following modules:

* File
* I/O
* Math
* Net
* OS
* Reflection
* Regex

#### Control flow ####

##### if statements #####

{% highlight ruby %}
if (bar()) {

}
{% endhighlight %}

##### for statements #####

{% highlight ruby %}
for (Int i = 0; i < 10; ++i) {

}
{% endhighlight %}

#### Function syntax ####

{% highlight ruby %}
Int foo(Int bar) {
	return bar;
}
{% endhighlight %}

#### Importing module ####

{% highlight ruby %}
import std.io;
import std.regex as re;
{% endhighlight %}
