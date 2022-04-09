=========
Constants
=========

**************
General Syntax
**************
When using the KCExpr class, constants follow a simple syntax: [<constant_code>] e.g. ``[levy]``. 
There is a finite list of mathematical constants that are recognised as constants by KCExpr.

.. list-table:: 
   :widths: 4 1
   :header-rows: 1

   * - Constant
     - Code

   * - Pi
     - pi
   * - Euler's Number
     - e
   * - Euler–Mascheroni constant
     - em
   * - The golden ratio
     - golden
   * - Meissel-Mertens constant
     - mm
   * - Bernstein's constant
     - bernstein
   * - Gauss-Kuzmin-Wirsing constant
     - gkw
   * - Hafner-Sarnak-McCurley constant
     - hsm
   * - Omega constant
     - omega
   * - Golomb-Dickman constant
     - gd
   * - Cahen's constant
     - cahen
   * - The twin prime constant
     - tp
   * - The laplace limit
     - laplace
   * - Embree-Trefethen constant
     - et
   * - Landau-Ramanujan constant
     - lr
   * - Brun's constant for prime quadruplets
     - brunpq
   * - Brun's constant for prime twins
     - brunpt
   * - Catalan's constant
     - catalan
   * - Viswanath's constant
     - viswanath
   * - Apéry's constant
     - apery
   * - Conway's constant
     - conway
   * - Mills' constant
     - mills
   * - The plastic number
     - plastic
   * - Ramanujan-Soldner constant
     - rs
   * - Backhouse's constant
     - backhouse
   * - Porter's constant
     - porter
   * - Lieb's square ice constant
     - lieb
   * - Erdős–Borwein constant
     - eb
   * - Niven's constant
     - niven
   * - The universal parabolic constant
     - upc
   * - Feigenbaum's α constant
     - feigenbauma
   * - Feigenbaum's δ constant
     - feigenbaumd
   * - Sierpinski's constant
     - sierpinski
   * - Khinchin's constant
     - khinchin
   * - Fransén–Robinson constant
     - fr
   * - Lévy's constant
     - levy
   * - The reciprocal Fibonacci constant
     - rf

******************************
Using constants in expressions
******************************

To use constants in expressions, simply include their syntax correctly within the expression. Examples:

.. code-block:: python
 
 import KCMath
 
 p = KCMath.KCExpr()
 p.set_expr("10/[laplace]")
 result = p.parse()
 print(result)  # prints "15.088795615383189" to the console

.. code-block:: python
 
 import KCMath
 
 p = KCMath.KCExpr()
 p.set_expr("pi(1,5,[fr]#)")
 result = p.parse()
 print(result)  # prints "20940.598039025044" to the console
