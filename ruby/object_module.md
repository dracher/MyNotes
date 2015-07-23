## 1. Resolving Ambiguous Method Names in MIX-IN
One of the other questions folks ask about mixins is, how is method lookup handled? In
particular, what happens if methods with the same name are defined in a class, in that class’s
parent class, and in a mixin included into the class?

The answer is that Ruby looks first in the immediate class of an object, then in the mixins
included into that class, and then in superclasses and their mixins. If a class has multiple
modules mixed in, the `last one` included is searched first.




## 2. Quotes

**Just because this idiom is common doesn’t make it good design**