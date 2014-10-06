cluss
=====

**simple alternative to type classes**

A *cluss* enables you to achieve function overloading, or ad-hoc polymorphism,
without creating a new type class.

In order to give ad-hoc polymorphism to a type variable `a`,
you simply use `In` with a list of "type patterns" like `In [Type T, ...] a`,
which indicates that the type matches some of the patterns;
which is analogous to a type class indicating that a type matches some of its "instances".
The constraint `In [Type T, ...] a` is what we call a "cluss".

Clusses can easily be used in a nested way
and even be *recursive*;
therefore, they are expressive enough to imitate Haskell-98-style type classes.

Clusses, however, go beyond a mere alternative to type classes.
They have *closed* and *prioritized* instances and *open* methods,
while type classes have open and unprioritized instances and closed methods.
Those properties give clusses the advantages different from type classes:

* You can judge whether a type `a` belongs to a cluss `In as`,
    on some level, writing `Has as a`,
    since cluss instances are closed.

* You can make cluss instances more flexibly,
    without causing overlapping instances or incoherent instances,
    since cluss instances are prioritized.

* You can create new methods for clusses anywhere in any module,
    since cluss methods are open.

More information can be found in the [hackage's haddock](http://hackage.haskell.org/package/cluss) or the [http://kinokkory.github.io/cluss/](updated haddock).

The latest version is available at [https://hackage.haskell.org/package/cluss](https://hackage.haskell.org/package/cluss).
