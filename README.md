Download Link: https://assignmentchef.com/product/solved-csci316-assignment3
<br>
<ol>

 <li>Define a LISP function MIN-2 with the following properties. MIN-2 takes two arguments,       A and B. If the arguments A and B are numbers such that A ≤ B, then MIN-2 returns A. If A       and B are numbers such that A &gt; B, then MIN-2 returns B.  If A or B is not a number, then       MIN-2 returns the symbol ERROR.</li>

</ol>

<h1>     Examples: (MIN-2  21.3  7/2)    =&gt; 7/2                   (MIN-2 17.5 29)    =&gt; 17.5                            (MIN-2    5   ‘APPLE) =&gt; ERROR      (MIN-2 ‘(31) ‘(54)) =&gt; ERROR</h1>

2.<strong>[Exercise 4 on p. 72 of Wilensky]</strong>  Write a LISP function SAFE-AVG that takes 2 arguments       and returns the average of those arguments if they are numbers.  If one or both of the arguments       is not a number, the function should return NIL.




<h1>      Examples: (SAFE-AVG  23  47.4) =&gt; 35.2            (SAFE-AVG  3  8) =&gt; 11/2                          (SAFE-AVG ‘(23.1) 47.3) =&gt; NIL   (SAFE-AVG ‘ORANGE ‘PLUM) =&gt; NIL</h1>




3.<strong>[Exercise 2 on p. 72 of Wilensky]</strong><em>  </em>Write a LISP predicate ODD-GT-MILLION that takes one       argument, and which returns T if its argument is an odd integer greater than a million, but returns       NIL otherwise.   Hint: Make use of the predicate INTEGERP. <em>       </em>Examples:

<h1>       (ODD-GT-MILLION 92010231) =&gt; T  (ODD-GT-MILLION 17) =&gt; NIL  (ODD-GT-MILLION 92010232) =&gt; NIL                  (ODD-GT-MILLION 21/5) =&gt; NIL                 (ODD-GT-MILLION 1718671.24) =&gt; NIL           (ODD-GT-MILLION ‘(2010231)) =&gt; NIL      (ODD-GT-MILLION ‘APPLE) =&gt; NIL</h1>




4.<strong>[Exercise 3 on p. 72 of Wilensky]</strong> Re-read the discussion of MEMBER in sec. 6.6 of Touretzky       or on p. 51 of Winston &amp; Horn. Then write a LISP predicate MULTIPLE-MEMBER that takes       two arguments and behaves as follows:  If the first argument is a symbol or number and the       second is a list, then MULTIPLE-MEMBER returns a <em>true</em> value if the first argument occurs at       least twice in the second argument, and returns NIL otherwise.




<h1>      Examples:  (MULTIPLE-MEMBER ‘A ‘(B A B B A C A D)) =&gt; (A C A D)                          (MULTIPLE-MEMBER ‘A ‘(B A B B C C A D)) =&gt; (A D)                                                 (MULTIPLE-MEMBER ‘A ‘(B A B B C D)) =&gt; NIL</h1>




[Notice that the behavior of MULTIPLE-MEMBER is unspecified in cases where the first      argument is not a symbol or number, and in cases where the second argument is not a list.  In       other words, your definition may return any value or produce an evaluation error in such cases.]




<ol start="5">

 <li>Define a LISP function MONTH-&gt;INTEGER which takes as argument a symbol that should be the name of a month, and which returns the number of the month.  For example:</li>

</ol>

(MONTH-&gt;INTEGER ‘MARCH) =&gt; 3         (MONTH-&gt;INTEGER ‘JUNE) =&gt; 6

If the argument is not a symbol that is the name of a month, the function should return the symbol       ERROR.  For example:

(MONTH-&gt;INTEGER ‘C) =&gt; ERROR              (MONTH-&gt;INTEGER 7) =&gt; ERROR

(MONTH-&gt;INTEGER ‘QUOTE) =&gt; ERROR    (MONTH-&gt;INTEGER ‘(MAY)) =&gt; ERROR




<ol start="6">

 <li>Define a LISP function SCORE-&gt;GRADE which takes a single argument, s, and returns a symbol according to the following scheme:</li>

</ol>

s ≥ 90                A                                73 ≤ s &lt; 77       C+                 87 ≤ s &lt; 90       A–                              70 ≤ s &lt; 73       C

83 ≤ s &lt; 87       B+                            60 ≤ s &lt; 70       D

80 ≤ s &lt; 83       B                                 s &lt; 60              F

77 ≤ s &lt; 80       B–

If the argument s is not a number then the function should return NIL.




<h1>      Examples:  (SCORE-&gt;GRADE 86.3) =&gt; B+   (SCORE-&gt;GRADE 106) =&gt; A    (SCORE-&gt;GRADE –10.1) =&gt; F                          (SCORE-&gt;GRADE 59.9) =&gt; F      (SCORE-&gt;GRADE 83) =&gt; B+    (SCORE-&gt;GRADE 74) =&gt; C+                          (SCORE-&gt;GRADE 67) =&gt; D              (SCORE-&gt;GRADE 87.0) =&gt; A–                                           (SCORE-&gt;GRADE ‘(86.3)) =&gt; NIL    (SCORE-&gt;GRADE ‘DOG) =&gt; NIL</h1>













Solve problems 7, 8, and 9 below <strong><u>without</u></strong> using COND, IF, WHEN, UNLESS, or CASE.




<ol start="7">

 <li>Define a LISP function GT with the following properties. GT takes two arguments. It returns T if the arguments are numbers and the first argument is greater than the second; otherwise it returns NIL.</li>

</ol>

<h1>      Examples:  (GT  0  –1) =&gt; T     (GT  –3  –7) =&gt; T     (GT  40  40) =&gt; NIL     (GT  ‘B  ‘A) =&gt; NIL</h1>




<ol start="8">

 <li>Define a LISP function SAME-PARITY with the following properties. SAME-PARITY takes       two arguments.  It returns T if both arguments are even integers or if both arguments are odd       integers.  In <em>all</em> other cases SAME-PARITY returns NIL.</li>

</ol>

<h1>     Examples:  (SAME-PARITY  0  –1) =&gt; NIL    (SAME-PARITY  –3  –9) =&gt; T     (SAME-PARITY  30  90) =&gt; T                           (SAME-PARITY  ‘A ‘A) =&gt; NIL    (SAME-PARITY  4.1  3.7) =&gt; NIL</h1>




<ol start="9">

 <li>Define a LISP function SAFE-DIV with the following properties. SAFE-DIV takes two arguments.      If both arguments are numbers and the second does not satisfy ZEROP, then the function returns the       result of dividing the first argument by the second. In <em>all</em> other cases it returns NIL.</li>

</ol>

<h1>     Examples:  (SAFE-DIV  6  4) =&gt;  3/2       (SAFE-DIV  6.0  4) =&gt;  1.5    (SAFE-DIV  6  0) =&gt;  NIL                         (SAFE-DIV  6  0.0) =&gt;  NIL   (SAFE-DIV  ‘(6)  4) =&gt;  NIL (SAFE-DIV  6  T) =&gt;  NIL</h1>

<strong> </strong>