Download Link: https://assignmentchef.com/product/solved-programming-problem3-functional-programming-with-haskell
<br>
<h1><u>Problem 1</u>: Basics of Haskell</h1>

<ol>

 <li><em>Working with ‘List’ in Haskell</em>: Define a function <em>m</em> that takes a lists of lists of integers and sums the numbers in each of the innermost lists together before multiplying the resulting sums with each other. For example,</li>

</ol>

*Main&gt; m [[1,2],[3,5]]

24

*Main&gt; m [[1,2,3],[7]]

42

*Main&gt; m [[7,8],[]]

0

*Main&gt; m [[1,2],[2,3],[4,5,6]]

225




<ol>

 <li><em>Working with ‘Basic Functions’ in Haskell</em>: Write a function called greatest, which has the following signature:</li>

</ol>

greatest :: (a -&gt; Int) -&gt; [a] -&gt; a




greatest f seq returns the item in seq that maximizes function f. For example:




*Main&gt; greatest sum [[2,5], [-1,3,4], [2]]

[2,5]




*Main&gt; greatest length [“the”, “quick”, “brown”, “fox”]   “quick”




*Main&gt; greatest id [51,32,3]

51




NB: If more than one item maximizes f, then greatest f returns the <em>first</em> one.




<ol>

 <li><em>Custom List Data Type</em>: Implement toList :: [a] -&gt; List a, which converts a regular Haskell list to a <sub>List a</sub>; and vice versa. For example,</li>

</ol>

*Main&gt; toList []

Empty




*Main&gt; toList [2, 7, 4]

Cons 2 (Cons 7 (Cons 4 Empty))




*Main&gt; toList “apple”

Cons ‘a’ (Cons ‘p’ (Cons ‘p’ (Cons ‘l’ (Cons ‘e’ Empty))))




AND

*Main&gt; toHaskellList Empty

[]




*Main&gt; toHaskellList (Cons 2 (Cons 7 (Cons 4 Empty)))

[2,7,4]




*Main&gt; toHaskellList (Cons “cat” (Cons “bat” (Cons “rat” Empty)))         [“cat”,”bat”,”rat”]

<strong> </strong>

<h1><u>Problem 2</u>: Anagram</h1>




Once Dylan and Lynda are playing with cards made by themselves only. Each card has some letter written on it and let us assume they have made enough cards so that they will not cause any limit in this game.

Now Dylan and Lynda bring up their own cards and they put all the cards on the table.  Let’s say Dylan brought up 3 cards and Lynda brought up only one card.

Dylan has 3 cards namely ‘X’, ‘Y’, ‘Y ’and Lynda has brought ‘X ’(order is important) Together they have ‘X’, ‘Y’, ‘Y, ‘X’.




Now, if you have observed then you would have noticed both of them has special characteristic in their names. Both names can form Anagrams (Dylan and Lynda) hence they always love anagram pairs. Now in these cards they decided to count total anagram subset of cards.




For Eg. here total 4 anagram subsets are possible (X, X), (Y, Y), (XY, XY), (XYY, YYX) (Remember they have followed order of the cards).

Since they both are very lazy it’s your job to help them to find total anagram subsets in the cards.

<strong> </strong>

<strong><u>Example</u></strong><strong>: </strong>




*Anagram&gt; [[‘x’, ‘y’], [‘x’, ‘y’]]

5

<em>Explanation: 6 possible anagram pairs after joining the both strings are: (x, x), (y, y), (xy, xy), (xy, yx), (yx, xy) </em>

*Anagram&gt; [[‘x’, ‘y’, ‘y’], [‘x’]]

4

<em>Explanation: 4 possible anagram pairs after joining the both strings are: (x, x), (y, y), (xy, yx), (xyy, yyx) </em>

<strong> </strong>

<strong> </strong>

<h1><u>Problem 3</u>: IITG Football League</h1>




The IITG sports board has decided to promote a healthy campus lifestyle in the campus amongst the academic personal. So they have decided to inaugurate a yearly football league amongst the various academic departments of IITG. The event will start from 1st Nov to 7th Nov 2019. The sports board has received positive response from the campus residents. 12 teams have registered for the inaugural season out of which 11 teams are from different departments and 1 team is from the staff members. The tournament will be knock out in the first round followed by a league in the second round out of which top 4 teams will reach the playoffs

Write a program in Haskell to carry out the draw for the fixtures. Your program should consider the following

<ol>

 <li>The draw will be for the initial round only where each team will play only one match.</li>

 <li>Use acronyms of the registered teams as follows:</li>

</ol>

<table width="499">

 <tbody>

  <tr>

   <td width="52">Sl. No</td>

   <td width="282">Team</td>

   <td width="165">Acronym</td>

  </tr>

  <tr>

   <td width="52">1</td>

   <td width="282">Biosciences &amp; Bio-Engineering</td>

   <td width="165">BS</td>

  </tr>

  <tr>

   <td width="52">2</td>

   <td width="282">Chemical Engineering</td>

   <td width="165">CM</td>

  </tr>

  <tr>

   <td width="52">3</td>

   <td width="282">Chemistry</td>

   <td width="165">CH</td>

  </tr>

  <tr>

   <td width="52">4</td>

   <td width="282">Civil Engineering</td>

   <td width="165">CV</td>

  </tr>

  <tr>

   <td width="52">5</td>

   <td width="282">Computer Science &amp; Engineering</td>

   <td width="165">CS</td>

  </tr>

  <tr>

   <td width="52">6</td>

   <td width="282">Design</td>

   <td width="165">DS</td>

  </tr>

  <tr>

   <td width="52">7</td>

   <td width="282">Electronics and Electrical Engineering</td>

   <td width="165">EE</td>

  </tr>

  <tr>

   <td width="52">8</td>

   <td width="282">Humanities and Social Sciences</td>

   <td width="165">HU</td>

  </tr>

  <tr>

   <td width="52">9</td>

   <td width="282">Mathematics</td>

   <td width="165">MA</td>

  </tr>

  <tr>

   <td width="52">10</td>

   <td width="282">Mechanical Engineering</td>

   <td width="165">ME</td>

  </tr>

  <tr>

   <td width="52">11</td>

   <td width="282">Physics</td>

   <td width="165">PH</td>

  </tr>

  <tr>

   <td width="52">12</td>

   <td width="282">Staff Members</td>

   <td width="165">ST</td>

  </tr>

 </tbody>

</table>




<ol>

 <li>After the draw, generate the fixtures for the first round with date and time.</li>

 <li>The first round will commence from 1st to 3rd Nov 2019. Schedule the fixtures in this period only.</li>

 <li>There will be two matches per day. The first match will start at 9:30 AM and the second match will start at 7:30 PM</li>

 <li>Your program should be able to display the entire fixture, match details about any particular team and the next match details</li>

</ol>

<strong> </strong>

<strong> </strong>

<strong>Sample Input/ Output: </strong>

<strong> </strong>

<table width="239">

 <tbody>

  <tr>

   <td width="183">*Main&gt; fixture ‘all’</td>

   <td width="56"> </td>

  </tr>

  <tr>

   <td width="183">  CS vs PH   1-11</td>

   <td width="56"> 9:30</td>

  </tr>

  <tr>

   <td width="183">  MA vs ST    1-11—-—-</td>

   <td width="56"> 7:30</td>

  </tr>

  <tr>

   <td width="183">  CV vs DS     3-11 *Main&gt; fixture ‘DS’</td>

   <td width="56"> 7:30</td>

  </tr>

  <tr>

   <td width="183">  ME vs DS   3-11</td>

   <td width="56"> 7:30</td>

  </tr>

 </tbody>

</table>




*Main&gt; nextMatch 1  13.25   [This means what is the next match when

current date is 1/11 and current time is 1:15 PM]

MA vs ST       1-11 7:30

<strong> </strong>

<strong> </strong>

<strong> </strong>

<h1><u>Problem 4</u>: Puzzle Solving (40+10 Marks)</h1>




<strong>Part A (40 Marks):</strong> Assume that there is a 4×4 grid structure as shown in the Fig 1(A). Some of the cells in the grid have some symbols (from a set of 4 distinct symbols), others are blank. The objective of the puzzle is to fill in the blank cells with symbols from the set of the four symbols, in such a way that every row, every column and the four 2×2 corner blocks have exactly one occurrence of each symbol.




Fig 1(A): Example Input                              Fig 1B: Example Output




<strong>Input:</strong> A partially filled up grid structure like Fig 1(A), where each symbol should be used only once. There should be scope of providing user-input (for the partial filling).

<strong>Output</strong>: Not solvable / the solution like Fig 1(B).

<strong>Part B (10 Marks):</strong> Solve the same for a 9×9 grid. Like the earlier one, some of the cells in the grid have some symbols, whereas others are kept blank. However, this time the number of distinct symbols are 9 instead of 4. The objective is same as before, i.e., to fill in the blank cells with symbols from the set of the 9 symbols, in such a way that every row, every column and each of the nine 3×3 blocks, shown in Fig 1(C), has exactly one occurrence of each symbol.

<table width="216">

 <tbody>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

   <td width="24"> </td>

  </tr>

 </tbody>

</table>




Fig 1(C): 9×9 blocks and the 3×3 sub-blocks




<strong>Input:</strong> A partially filled up grid structure– there should be scope of providing user-input (for the filling).

<strong>Output</strong>: Not solvable / the solved puzzle<strong>.</strong>