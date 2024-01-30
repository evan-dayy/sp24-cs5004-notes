<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a>
    <img src="resources/logo.png" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Java OOD Related Q&A</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#acess-level-private-protected-private-protected-public">Access Level: private, protected-private, protected, public</a></li>
    <li><a href="#final-key-word">final key word</a></li>
    <li><a href="#equals-and">.equals and ==</a></li>
    <li><a href="#equals-and-hashcode">.equals and hashCode</a></li>
  </ol>
</details>

## Access Level: private, protected-private, protected, public

Access level defined **who** could access a class field or a method, in some scenario, you would like to protect data that cannot be changed from others. There are 4 access level in java, `private`, `public`, `proctected`, `protected-private`;

- `private` and `public` are the most extreme one, it stards for `no one` and `everyone` can see it; That is why we need `getter` and `setter` method for `private field` because there is no way you can access these fields unless you are inside that class;

- Then we have `protected-private`, which is the `default` setting if you do not explicitly specify the access level. It also allows all the other class within the same package to access this type;

- Then we have `protected`, which is almost the same as `protected-private` but it allows its subclasses outside the package have access to use this type of method;

## final key word

Same as what it suggests. `final` key word can apply to a class, a method, or a variable;

- if it apply to a class, like `final Employee`, it suggests the class cannot be subclass;

- if it apply to a method, it suggests the method cannot be over written;

- if it apply to a field, the field cannot be reassigned a value once initialized, and you must initialize it when you declare it;

## `.equals` and `==`

It is very important to understand the difference between the equality and identity of objects.

- Identity defines two objects as being ‘the same’ if they really are referring to the same, exact object.
- Equality, on the other hand, defines two objects as being ‘the same’ if they contain the same value(s).

`==` determines identity while `.equals` is for equality.

## `.equals` and `hashCode`

The idea `hashing` is the transformation of any object into a number. The transforming function is called a `hash function`, and the `int` return value is the hash value. In Java, `hash functions` are defined in the object’s class as a method called `hashCode()` with return value `int`;

Keep it really careful when you try to Override the `equals` method, since a old version of `hashcode` may cause `inconsistency` in hash table;
