``AnyMap``, a safe and convenient store for one value of each type
==================================================================

[![Build Status](https://travis-ci.org/chris-morgan/anymap.svg?branch=master)](https://travis-ci.org/chris-morgan/anymap)

If you’re familiar with Go and Go web frameworks, you may have come across the common “environment” pattern for storing data related to the request. It’s typically something like ``map[string]interface{}`` and is accessed with arbitrary strings which may clash and type assertions which are a little unwieldy and must be used very carefully.

This is madness. Hare-brained, stark, raving madness, just *asking* for things to blow up in your face. Unfortunately for people in Go, it’s the best that they can have because of its weak type system; such a thing cannot possibly be made safe without generics.

Fortunately, we can do better in Rust. Our type system is quite equal to easy, robust expression of such problems.

The ``AnyMap`` type is a friendly wrapper around a ``HashMap<TypeId, Box<Any>:'static>``, exposing a nice, easy typed interface, perfectly safe and absolutely robust.

What this means is that in an ``AnyMap`` you may store zero or one values for every type.

Instructions
------------

    make

Future work
-----------

I think that the only thing left for this is filling out additional methods from ``HashMap`` as appropriate.

It’s a very simple thing.

Author
------

[Chris Morgan](http://chrismorgan.info/) ([chris-morgan](https://github.com/chris-morgan)) is the primary author and maintainer of AnyMap.

License
-------

This library is distributed under similar terms to Rust: dual licensed under the MIT license and the Apache license (version 2.0).

See LICENSE-APACHE, LICENSE-MIT, and COPYRIGHT for details.