---
layout: post
---

#### Code Samples ####
Here you can find some code samples written in Clever.

#### TCP Sockets

{% highlight ruby %}
// This TcpSocket example simulates a HTTP 1.1 request against a valid IP 
// address on the Internet, showing the HTML source of the page.

import std.io;
import std.net;

Int i = 8;
String page;

TcpSocket s = TcpSocket();
s.setHost("200.132.43.5");
s.setPort(80);
s.connect();

s.send("GET / HTTP/1.1\n");
s.send("Host: 200.132.43.5\n");
s.send("\n");

while (i > 0) {
    page = s.receive();
    print(page);

    if (!s.poll()) {
        i--;
    }
}

println("-- Finished. --");
{% endhighlight %}

#### Sieve of Erastothenes

{% highlight ruby %}
// Fills an Array<Int> named `primes` with all primes less than 1000

import std.io as io;

Array<Bool> isPrime;
isPrime.resize(1000, true);
isPrime.set(0, false);
isPrime.set(1, false);

// Setting all even > 2 to false
for (Int i = 4; i < 1000; i += 2) {
	isPrime.set(i, false);
}

// This array will contain all primes < SIZE
Array<Int> primes;
primes.push(2);

for (Int i = 3; i < isPrime.size(); i += 2) {
	if (isPrime.at(i)) {
		primes.push(i);
		
		for (Int j = i + i; j < isPrime.size(); j += i) {
			isPrime.set(j, false);
		}
	}
}

// prints the primes
for (Int i = 0; i < primes.size(); ++i) {
	io::print(primes.at(i), ' ');
}

io::print("\n");
{% endhighlight %}
