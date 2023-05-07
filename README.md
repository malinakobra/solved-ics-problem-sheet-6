Download Link: https://assignmentchef.com/product/solved-ics-problem-sheet-6
<br>
<table width="572">

 <tbody>

  <tr>

   <td width="201"><strong>Problem 6.1: </strong><em>long life diet rules</em></td>

   <td width="248"> </td>

   <td width="123"> </td>

  </tr>

 </tbody>

</table>

Uwe Schonig published in his book “Logic for Computer Scientists” the following little story:¨

A 100 year old was asked “What is the secret of having a long life?” and he did respond to stick to three diet rules:

<ol>

 <li>If you don’t take beer, you must have fish.</li>

 <li>If you have both beer and fish, don’t have ice cream.</li>

 <li>If you have ice cream or don’t have beer, then don’t have fish.</li>

</ol>

The questioner found this answer quite confusing. Can you help to simplify the answer?

We introduce three boolean variables: The variable <em>B </em>is true if we have beer, the variable <em>F </em>is true if we have fish, and the variable <em>I </em>is true if we have ice cream.

<ol>

 <li>Provide a boolean formula for the function <em>D</em>(<em>B,F,I</em>) that captures the three rules.</li>

 <li>Construct a truth table that shows all interpretations of <em>D</em>(<em>B,F,I</em>). Break things into meaningful steps so that we can award partial points in case things go wrong somewhere.</li>

 <li>Out of the truth table, derive a simpler boolean formula defining <em>D</em>(<em>B,F,I</em>).</li>

 <li>Take the boolean formula from a) and algebraically derive the simpler boolean formula from c). Annotate each step of your derivation with the equivalence law that you apply so that we can follow along.</li>

</ol>

<strong>Problem 6.2: </strong><em>long life diet rules                                                                                                          </em>

Uwe Schonig published in his book “Logic for Computer Scientists” the following little story:¨

A 100 year old was asked “What is the secret of having a long life?” and he did respond to stick to three diet rules:

<ol>

 <li>If you don’t take beer, you must have fish.</li>

 <li>If you have both beer and fish, don’t have ice cream.</li>

 <li>If you have ice cream or don’t have beer, then don’t have fish.</li>

</ol>

The questioner found this answer quite confusing. Can you help to simplify the answer?

We introduce three boolean variables: The variable <em>B </em>is true if we have beer, the variable <em>F </em>is true if we have fish, and the variable <em>I </em>is true if we have ice cream.

<ol>

 <li>Define a function</li>

</ol>

diet :: Bool -&gt; Bool -&gt; Bool -&gt; Bool

that implements the three diet rules directly following the description given above and a function

diet’ :: Bool -&gt; Bool -&gt; Bool -&gt; Bool

that implements a simplified diet formula.

<ol>

 <li>Define a function truthTable :: (Bool -&gt; Bool -&gt; Bool -&gt; Bool) -&gt; [(Bool, Bool, Bool, Bool)]</li>

</ol>

takes a (diet) function as an argument and returns a list where each element is a 4-tuple representing three input values passed to the (diet) function followed by the function’s result.

Submit your Haskell code as a plain text file.

Below is a unit test template that you can use to fill in your code.

1 module Main (main) where

2

3 import Test.HUnit

4

<ul>

 <li><em>— The function diet implements the three diet rules directly.</em></li>

 <li>diet :: Bool -&gt; Bool -&gt; Bool -&gt; Bool</li>

 <li>diet b f i = undefined</li>

</ul>

8

<ul>

 <li><em>— The function diet’ implements the simplified diet formula.</em></li>

 <li>diet’ :: Bool -&gt; Bool -&gt; Bool -&gt; Bool</li>

 <li>diet’ b f i = undefined</li>

</ul>

12

<ul>

 <li><em>— The function truthTable takes a function as an argument and returns</em></li>

 <li><em>— a list where each element is a 4-tuple representing three input </em>15 <em>— value passed to the function followed by the function’s result.</em></li>

 <li>truthTable :: (Bool -&gt; Bool -&gt; Bool -&gt; Bool) -&gt; [(Bool, Bool, Bool, Bool)]</li>

 <li>truthTable f = undefined</li>

</ul>

18

19 <em>— Test whether the two truth tables returned are the same (which is </em>20 <em>— not a very sharp test but I do not want to reveal too many details).</em>

<ul>

 <li><em>— You may want to add your own test cases…</em></li>

 <li>dietTests = TestList [ truthTable diet ~?= truthTable diet’ ]</li>

</ul>

23

24 main = runTestTT dietTests