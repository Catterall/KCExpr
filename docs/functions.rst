=========
Functions
=========

**************
General Syntax
**************
When using the KCExpr class, functions follow a simple syntax: <func_name>(<func_expr>) e.g. ``sin(0.5)``. 
There is a finite list of mathematical functions that are recognised as functions by KCExpr.

.. list-table:: 
   :widths: 1 6
   :header-rows: 1

   * - Function
     - Usage

   * - ``abs(x)``
     - The absolute function returns a numbers distance from 0 e.g. ``abs(-7)`` returns ``7.0``.
   * - ``sqrt(x)``
     - The square root function returns the square root of a number e.g. ``sqrt(4)`` returns ``2.0``.
   * - ``root(x,n)``
     - The root function returns the nth root of a number e.g. ``root(8,3)`` returns ``2.0``.
   * - ``ncr(n,r)``
     - The nCr function returns the number from Pascal's triangle at row n, column r e.g. ``ncr(5,2)`` returns ``10.0``.
   * - ``npr(n,r)``
     - The nPr function returns the permutation of arrangement of 'r' objects from a set of 'n' objects, into an order or sequence e.g. ``npr(5,3)`` returns ``60.0``.
   * - ``sigma(i,n,expr)``
     - The sigma function returns the summation of an expression, where the var operator is from i to n e.g. ``sigma(1,5,#)`` returns ``15.0``. **In KCExpr, the variable operator is #**.
   * - ``pi(i,n,expr)``
     - The pi function returns the product of an expression, where the var operator is from i to n e.g. ``pi(1,5,#)`` returns ``120.0``. **In KCExpr, the variable operator is #**.
   * - ``ln(x)``
     - The natural logarithm function returns the logarithm of a number to the base e e.g. ``ln(10)`` returns ``2.30...``
   * - ``log(x,b)``
     - The logarithm function returns the logarithm of a number to the base b e.g. ``log(10,2)`` returns ``3.32...``
   * - ``sin(x)``
     - The sine function returns the sine of a number radians e.g. ``sin(0.5)`` returns ``0.47...``
   * - ``sina(x)``
     - The arcsine function returns the arcsine of a number radians e.g. ``sina(0.5)`` returns ``0.52...``
   * - ``csc(x)``
     - The cosecant function returns the cosecant of a number radians e.g. ``csc(0.5)`` returns ``2.08...``
   * - ``sinh(x)``
     - The hyperbolic sine function returns the hyperbolic sine of a number radians e.g. ``sinh(0.5)`` returns ``0.52...``
     - ``csch(x)``
     - The hyperbolic cosecant function returns the hyperbolic cosecant of a number radians e.g. ``csch(0.5)`` returns ``1.91...``
     - ``sinha(x)``
     - The arc-hyperbolic sine function returns the arc-hyperbolic sine of a number radians e.g. ``sinha(0.5)`` returns ``0.48...``
   * - ``cos(x)``
     - The cosine function returns the cosine of a number radians e.g. ``cos(0.5)`` returns ``0.87...``
   * - ``cosa(x)``
     - The arccosine function returns the arccosine of a number radians e.g. ``cosa(0.5)`` returns ``1.04...``
   * - ``sec(x)``
     - The secant function returns the secant of a number radians e.g. ``sec(0.5)`` returns ``1.13...``
   * - ``cosh(x)``
     - The hyperbolic cosine function returns the hyperbolic cosine of a number radians e.g. ``cosh(0.5)`` returns ``1.12...``
     - ``sech(x)``
     - The hyperbolic secant function returns the hyperbolic secant of a number radians e.g. ``sech(0.5)`` returns ``0.88...``
     - ``cosha(x)``
     - The arc-hyperbolic cosine function returns the arc-hyperbolic cosine of a number radians e.g. ``cosha(10.0)`` returns ``2.99...``
   * - ``tan(x)``
     - The tangent function returns the tangent of a number radians e.g. ``tan(0.5)`` returns ``0.54...``
   * - ``atan(x)``
     - The arctangent function returns the arctangent of a number radians e.g. ``atan(0.5)`` returns ``0.46...``
   * - ``cot(x)``
     - The cotangent function returns the cotangent of a number radians e.g. ``cot(0.5)`` returns ``1.83...``
   * - ``tanh(x)``
     - The hyperbolic tangent function returns the hyperbolic tangent of a number radians e.g. ``tanh(0.5)`` returns ``0.46...``
     - ``coth(x)``
     - The hyperbolic cotangent function returns the hyperbolic cotangent of a number radians e.g. ``coth(0.5)`` returns ``2.16...``
     - ``tanha(x)``
     - The arc-hyperbolic tangent function returns the arc-hyperbolic tangent of a number radians e.g. ``tanha(0.5)`` returns ``0.54...``
   * - ``x! (and gamma)``
     - Whilst an operator, not a function, the factorial does utilize the gamma function. ``x!`` returns ``math.gamma(x+1)``.
       
       This can also be utilized get the gamma of x: ``(x-1)!`` returns ``math.gamma(x)``.

******************************
Using functions in expressions
******************************

To use functions in expressions, simply include their syntax correctly within the expression. Examples:

.. code-block:: python
 
 import KCExpr.KCExpr as kce
 
 p = kce.KCExpr()
 p.set_expr("sin(0.5)+cos(0.5)-log(10,3)")
 result = p.parse()
 print(result)  # prints "-0.7388951738" to the console

.. code-block:: python
 
 import KCExpr
 
 p = kce.KCExpr()
 p.set_expr("sigma(2,10,log(50,#))")
 result = p.parse()
 print(result)  # prints "24.01175518" to the console
