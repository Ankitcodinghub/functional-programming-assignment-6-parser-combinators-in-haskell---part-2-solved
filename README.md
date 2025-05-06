# functional-programming-assignment-6-parser-combinators-in-haskell---part-2-solved
**TO GET THIS SOLUTION VISIT:** [Functional-Programming Assignment 6-Parser combinators in Haskell – Part 2 Solved](https://www.ankitcodinghub.com/product/functional-programming-assignment-6-parser-combinators-in-haskell-part-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;97104&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Functional-Programming Assignment 6-Parser combinators in Haskell - Part 2 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Lab 12

Parser combinators in Haskell – Part 2

Goals

In this lab you will learn to:

1. Understand LISP syntax

2. Write a parser for a subset of LISP

</div>
</div>
<div class="layoutArea">
<div class="column">
Resources

Resource

An intuition for LISP syn- tax

COMMON LISP: A Gentle In- troduction to Symbolic Com- putation

Structure and Interpreta- tion of Computer Pro- grams

Functional parsing

Understanding parser combinators

Understanding parser combi- nators: a deep dive – Scott Wlaschin

</div>
<div class="column">
Table 12.1: Lab Resources

Link

<pre>https://stopa.io/post/265
https://www.cs.cmu.edu/~dst/LISPBook/book.pdf
</pre>
<pre>https://opendocs.github.io/sicp/sicp.pdf
</pre>
<pre>https://youtu.be/dDtZLm7HIJs
</pre>
https://fsharpforfunandprofit.com/posts/understanding-parser-combinators/

<pre>https://www.youtube.com/watch?v=RDalzi7mhdY
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
129

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
12.1 Intro to LISP

12.1.1 Polish notation (prefix notation)

Concept 12.1.1: Polish notation (prefix notation)

Polish notation or Prefix notation is a way to write mathematical or logical expressions, where the operator is before the operands. For example instead of writing 1 + 2, we write + 1 2 and instead of (2−1)+(3∗4) we write + − 2 1 ∗ 3 4. Notice that with this notation, we can omit all parentheses without introducing any ambiguity, though we can still use parentheses to improve clarity: + (− 2 1) (∗ 3 4).

You’ve already used this notation with almost all programming languages, where function calls use prefix notation (since infix notation works only for binary functions). Thus in this style, we would write a function call as: fabc, where f is the name of the function and a,b,c are its parameters.

If we want to call multiple functions, we can use the same notation, but with parentheses: f (g a b) (h a) c , which you’ve already seen while using Elm, Haskell and SML! Instead of placing the arguments in parentheses and after the function name, we place the function name

and the arguments between the parentheses, with the function name being the first element.

12.1.2 LISP programs

LISP is a very simple, yet powerful language: a program is just a nested list of expressions. Expressions can be lists or atoms, which are numbers or symbols (identifiers). This allows LISP programs to be also considered as data, that can be manipulated by the program itself in a similar fashion to reflection in Java.

For example, the following are all valid LISP expressions: (+ 1 2) , (+ 1 2 3) . In each case, + is the first element in the list and it corresponds to a function call with an arbitrary num- ber of arguments. We can also use multiple functions, using parentheses to denote function

application: (+(-21)(*123)).

The final aspect is that because the program is actually also data, we need a way to differentiate between code that we want to be executed (i.e. function to be called on its arguments) and data definition. To mark a list or a symbol as data, we use quoting, with the ’ character. For example, to create the equivalent of the following Haskell list [1, 2, 3] in LISP, we write

’(1 2 3) , which means that this expression shouldn’t be evaluated (i.e. don’t treat 1 as function applied on 2 and 3 ).

Now that we can define lists as data, we can also define functions to manipulate lists: car , which returns the first element of a list and cdr , which skips the first element and returns rest of the elements of the list. So (car ’(1 2 3)) is 1, (cdr ’(1 2 3)) is (2 3) and (car (cdr ’(1 2 3))) is 2.

</div>
</div>
<div class="layoutArea">
<div class="column">
130

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
12.2 Assignment

</div>
</div>
<div class="layoutArea">
<div class="column">
Deadline: Monday, January 11, 23:55

12.3 Submission instructions

<ol>
<li>Unzip the MiniLisp.zip folder. You should find: ❼ 2 files in the src folder:
– Parser.hs – for the basic parsing library that you completed at the last lab

– MiniLisp.hs – for the LISP parser that you partially completed at the last lab
</li>
<li>Edit the first line of each of the source files as described in the comments.</li>
<li>Edit the source files in the src folder with your solutions.</li>
<li>When done, zip this MiniLisp folder and name the zip archive with the following format:
MiniLisp ⟨FirstName⟩ ⟨LastName⟩ ⟨Group⟩

Examples of valid names:

❼ MiniLisp John Doe 30432.zip

❼ MiniLisp Ion Popescu 30434.zip

❼ MiniLisp Gigel-Dorel Petrescu 30431.zip

Examples of invalid names:

❼ Solutions.zip

❼ MiniLisp.zip

❼ Solutii MiniLisp Ion Popescu.zip
</li>
</ol>
12.3.1 Preparation

Update your existing MiniLisp.hs file from the previous lab by adding the new definitions from the MiniLisp.hs file from this lab.

12.3.2 Exercises

Exercise 12.3.1 3p Create a parser sepBy sep p with the signature sepBy :: Parser a -&gt; Parser b -&gt; Parser [b]

</div>
</div>
<div class="layoutArea">
<div class="column">
131

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
<pre>   &gt; runParser (sepBy (char ’,’) ident) "a,b,c"
   Success ["a", "b", "c"] ""
   &gt; runParser (sepBy (char ’,’) ident) "abc"
   Success ["abc"] ""
</pre>
<pre>   &gt; runParser (sepBy (char ’,’) ident) "a,,b"
   Success ["a"] ",,b"
   &gt; runParser (sepBy ws ident) "a  b c     d"
   Success ["a", "b", "c", "d"] ""
</pre>
Exercise 12.3.2

</div>
<div class="column">
2p

</div>
</div>
<div class="layoutArea">
<div class="column">
Haskell REPL

</div>
</div>
<div class="layoutArea">
<div class="column">
Create a parser lispAtom :: Parser lispAtom which parses a LISP atom (either number or symbol).

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>   &gt; runParser lispAtom "abc"
   Success (Symbol "abc") ""
   &gt; runParser lispAtom "123"
   Success (Number 123) ""
</pre>
Exercise 12.3.3

</div>
<div class="column">
2p

</div>
</div>
<div class="layoutArea">
<div class="column">
Haskell REPL

</div>
</div>
<div class="layoutArea">
<div class="column">
Create a parser lispList :: Parser [LispValue] which parses a list of LISP values, using the lisp function (that you will write in Exercise 12.3.4).

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>   &gt; runParser lispList "(a b c)"
   Success [Atom (Symbol "a"),Atom (Symbol "b"),Atom (Symbol "c")] ""
   &gt; runParser lispList "(a b c("
   Error "Unexpected character ’(’"
</pre>
Exercise 12.3.4

</div>
<div class="column">
2p

</div>
</div>
<div class="layoutArea">
<div class="column">
Create a parser lisp :: Parser LispValue which parses a LISP value, using the lispAtom and lispList functions.

Haskell REPL

<pre>   &gt; runParser lisp "(a b c)"
   Success (List [Atom (Symbol "a"),Atom (Symbol "b"),Atom (Symbol "c")]) ""
   &gt; runParser lisp "123"
   Success (Atom (Number 123)) ""
   &gt; runParser lisp "abc1"
   Success (Atom (Symbol "abc1")) ""
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
Haskell REPL

</div>
</div>
<div class="layoutArea">
<div class="column">
132

</div>
</div>
</div>
