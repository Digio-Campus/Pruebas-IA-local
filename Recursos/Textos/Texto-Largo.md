CHAPTER 1

THE REAL AND COMPLEX NUMBER SYSTEMS

1.1 INTRODUCTION

Mathematical analysis studies concepts related in some way to real numbers, so
we begin our study of analysis with a discussion of the real-number system.
Several methods are used to introduce real numbers. One method starts with
the positive integers 1, 2, 3, ... as undefined concepts and uses them to build a
larger system, the positive rational numbers (quotients of positive integers), their
negatives, and zero. The rational numbers, in turn, are then used to construct the
irrational numbers, real numbers like √2 and π which are not rational. The rational and irrational numbers together constitute the real-number system.

Although these matters are an important part of the foundations of mathematics, they will not be described in detail here. As a matter of fact, in most
phases of analysis it is only the properties of real numbers that concern us, rather
than the methods used to construct them. Therefore,we shall take the real numbers
themselves as undefined objects satisfying certain axioms from which further
properties will be derived. Since the reader is probably familiar with most of the
properties of real numbers discussed in the next few pages, the presentation will
be rather brief. Its purpose is to review the important features and persuade the
reader that, if it were necessary to do so, all the properties could be traced back
to the axioms. More detailed treatments can be found in the references at the end
of this chapter.

For convenience we use some elementary set notation and terminology. Let
S denote a set (a collection of objects). The notation x ∈ S means that the object x
is in the set S, and we write x ∉ S to indicate that x is not in S.

A set S is said to be a subset of T, and we write S s T, if every object in S is
also in T. A set is called nonempty if it contains at least one object.

We assume there exists a nonempty set R of objects, called real numbers,
which satisfy the ten axioms listed below. The axioms fall in a natural way into
three groups which we refer to as the field axioms, the order axioms, and the
completeness axiom (also called the least-upper-bound axiom or the axiom of
continuity).

1.2 THE FIELD AXIOMS

Along with the-set R of real numbers we assume the existence of two operations,
called addition and multiplication, such that for every pair of real numbers x and y
the sum x + y and the product xy are real numbers uniquely determined by x
and y satisfying the following axioms. (In the axioms that appear below, x, y,
z represent arbitrary real numbers unless something is said to the contrary.)

- Axiom 1. x + y = y + x, xy = yx (commutative laws).
- Axiom 2. x + (y + z) = (x + y) + z, x(yz) = (xy)z (associative laws).
- Axiom 4. Given any two real numbers x and y, there exists a real number z such that
x + z = y. This z is denoted by y - x; the number x - x is denoted by 0. (It
can be proved that 0 is independent of x.) We write - x for 0 - x and call - x the
negative of x.
- Axiom 5. There exists at least one real number x ≠ 0. If x and y are two real
numbers with x ≠ 0, then there exists a real number z such that xz = y. This z is
denoted by y/x; the number x/x is denoted by 1 and can be shown to be independent of
x. We write x^-1 for 1/x if x ≠ 0 and call x^-1 the reciprocal of x.

From these axioms all the usual laws of arithmetic can be derived; for example,
-(-x)=x,(x^-1)^-1=x, -(x-y)=y-x,x-y=x+(-y),etc. (For
a more detailed explanation, see Reference 1.1.)

1.3 THE ORDER AXIOMS

We also assume the existence of a relation < which establishes an ordering among
the real numbers and which satisfies the following axioms:

- Axiom 6. Exactly one of the relations x = y, x < y, x > y holds.
    - NOTE. x > y means the same as y < x.
- Axiom 7. If x < y, then for every z we have x + z < y + z.
- Axiom 8. If x > 0 and y > 0, then xy > 0.
- Axiom 9. If x > y and y > z, then x > z.
    - NOTE. A real number x is called positive if x > 0, and negative if x < 0. We
denote by R+ the set of all positive real numbers, and by R- the set of all negative
real numbers.

From these axioms we can derive the usual rules for operating with inequalities.
For example, if we have x < y, then xz < yz if z is positive, whereas xz > yz if
z is negative. Also, if x > y and z > w where both y and w are positive, then
xz > yw. (For a complete discussion of these rules see Reference 1.1.)

NOTE. The symbolism x <= y is used as an abbreviation for the statement: x <= y or
x = y.


Thus we have 2 <= 3 since 2 < 3; and 2 <= 2 since 2 = 2. The symbol >= is
similarly used. A real number x is called nonnegative if x >= 0. A pair of simultaneous inequalities such as x < y, y < z is usually written more briefly as
x < y < z  

Theorem 1.1. Given real numbers a and b such that a <= b + ε, for every ε > 0 
Then a <= b. (1)

Proof. If b < a, then inequality (1) is violated for ε = (a - b)/2 because
b+ε= b + (a-b)/2 = a+b/2 < a + a=a
Therefore, by Axiom 6 we must have a <= b.

Axiom 10, the completeness axiom, will be described in Section 1.11.

1.4 GEOMETRIC REPRESENTATION OF REAL NUMBERS

The real numbers are often represented geometrically as points on a line (called
the real line or the real axis). A point is selected to represent 0 and another to
represent 1, as shown in Fig. I.I. This choice determines the scale. Under an
appropriate set of axioms for Euclidean geometry, each point on the real line
corresponds to one and only one real number and, conversely, each real number
is represented by one and only one point on the line. It is customary to refer to
the point x rather than the point representing the real number x.

The order relation has a simple geometric interpretation. If x < y, the point
x lies to the left of the point y, as shown in Fig. 1.1. Positive numbers lie to the
right of 0, and negative numbers to the left of 0. If a < b, a point x satisfies the
inequalities a < x < b if and only if x is between a and b.

1.5 INTERVALS

The set of all points between a and b is called an interval. Sometimes it is important
to distinguish between intervals which include their endpoints and intervals which
do not.

NOTATION. The notation {x: x satisfies P} will be used to designate the set of
all real numbers x which satisfy property P.

Definition 1.2. Assume a < b. The open interval (a, b) is defined to be the set
(a, b) = {x : a < x < b}. The closed interval [a, b] is the set {x: a <= x <= b}. The half-open intervals (a, b] and [a, b) are similarly defined, using the inequalities a < x <= b and a <= x < b, respectively. 

Infinite intervals are defined as follows:
(a, + ∞) = {x : x > a}, [a, + ∞) = {x : x >= a},
(- ∞, a) = {x: x < a}, (- ∞, a] = {x : x <= a}.

The real line R is sometimes referred to as the open interval (- ∞, + ∞). A
single point is considered as a "degenerate" closed interval.

NOTE. The symbols + ∞ and - ∞ are used here purely for convenience in notation
and are not to be considered as being real numbers. Later we shall extend the
real-number system to include these two symbols, but until this is done, the reader
should understand that all real numbers are "finite."
