Download Link: https://assignmentchef.com/product/solved-fit1045-algorithms-and-programming-in-python-s2-assignment-1
<br>
<h1>Objectives</h1>

The <strong>objectives of this assignment </strong>are:

<ul>

 <li>To demonstrate the ability to implement algorithms using basic data structures and operations on them.</li>

 <li>To gain experience in designing an algorithm for a given problem description and implementing that algorithm in Python.</li>

</ul>

<h1>Submission Procedure</h1>

<ol>

 <li>Save your files into a zip file called yourStudentID yourFirstName yourLastName.zip</li>

 <li>Submit your zip file containing your solution to Moodle.</li>

 <li>Your assignment will not be accepted unless it is a readable zip file.</li>

</ol>

<strong>Important Note: </strong>Please ensure that you have read and understood the university’s policies on plagiarism and collusion available at <a href="http://www.monash.edu.au/students/policies/academic-integrity.html">http://www.monash.edu.au/students/policies/academic-integrity.html</a><a href="http://www.monash.edu.au/students/policies/academic-integrity.html">.</a> You will be required to agree to these policies when you submit your assignment.

A common mistake students make is to use Google to find solutions to the questions. Once you have seen a solution it is often difficult to come up with your own version. The best way to avoid making this mistake is to avoid using Google. You have been given all the tools you need in workshops. If you find you are stuck, feel free to ask for assistance on Moodle, ensuring that you do not post your code.

<strong>Marks: </strong>This assignment will be marked both by the correctness of your code and by an interview with your lab demonstrator, to assess your understanding. This means that although the quality of your code (commenting, decomposition, good variable names etc.) will not be marked directly, it will help to write clean code so that it is easier for you to understand and explain.

This assignment has a total of 12 marks and contributes to 10% of your final mark. For each day an assignment is late, the maximum achievable mark is reduced by 10% of the total. For example, if the assignment is late by 3 days (including weekends), the highest achievable mark is 70% of 12, which is 8.4. Assignments submitted 7 days after the due date will normally not be accepted.

Detailed marking guides can be found at the end of each task. Marks are subtracted when you are unable to explain your code via a code walk-through in the assessment interview. <strong>Readable code is the basis of a convincing code walk-through.</strong>

<h1>Task 1: Strings (3.5 Marks)</h1>

Create a Python module called strings.py. Within this module implement the following three tasks. For this module you may <strong>not </strong>use the Python sequence method s.count(x). You may not import any other libraries or modules.

<h2>Part A: Code Breaker (1 Mark)</h2>

Write a function decode(string, n) that takes in an encoded message as a string and returns the decoded message.

<strong>Input</strong>: a string string and a positive integer n.

<strong>Output</strong>: the decoded string. The string is decoded by discarding the first n characters from the input string, keeping the next n characters, discarding the next n characters, and so on, until the input string is exhausted.

There is no guarantee at which point in the decoding (keep or discard) the string will be exhausted. There is no guarantee that the length of string will be a multiple of n.

<h3>Examples</h3>

<ol>

 <li>Calling decode(‘#P#y#t#h#o#n#’, 1) returns ‘Python’.</li>

 <li>Calling decode(‘AxYLet1x3’s T74codaa7e!’, 3) returns ‘Let’s code!’.</li>

</ol>

<h2>Part B: Pattern Finder (1 Mark)</h2>

Write a function pattern count(string, pat) that counts how many times a pattern occurs within a text.

<strong>Input</strong>: a string string and a non-empty string pat, both comprising both upper and lower case alphanumeric and non-alphanumeric characters.

<strong>Output</strong>: an integer count of the number of times pat occurs within string. The count is case sensitive. (See

Example c.)

<h3>Examples</h3>

<ol start="2">

 <li>Calling pattern count(‘bcabcabca’, ‘abc’) returns 2.</li>

 <li>Calling pattern count(‘aaaa’, ‘aa’) returns 3.</li>

 <li>Calling pattern count(‘A long time ago in a galaxy far, far away…’, ‘a’) returns 8.</li>

 <li>Calling pattern count(‘If you must blink, do it now.’, ‘code’) returns 0.</li>

</ol>

<h2>Part C: Palindromes (1.5 Marks)</h2>

A palindrome is a word, phrase, or sequence that reads the same backwards as forwards. Write a function palindrome(string) that determines whether or not a given string is a palindrome. In order to receive full marks, the function must determine whether the alphanumerical characters create a palindrome (see Examples). <strong>Input</strong>: a string string comprising both upper and lower case alphanumeric and non-alphanumeric characters.

<strong>Output</strong>: a boolean, True if the string when converted to lower case alphanumeric characters is a palindrome; otherwise False.

<h3>Examples</h3>

<ol>

 <li>Calling palindrome(‘RacecaR’) returns True because ‘RacecaR’ reads the same backwards as forwards.</li>

 <li>Calling palindrome(‘66racecar77’) returns False because ‘66racecar77’ does not read the same backwards as forwards.</li>

 <li>Calling palindrome(‘Racecar’) returns True because ‘racecar’ reads the same backwards as forwards.</li>

 <li>Calling palindrome(‘Madam, I’m Adam’) returns True because ‘madamimadam’ reads the same backwards as forwards.</li>

 <li>Calling palindrome(‘#4Satire: Veritas4’) returns True because ‘4satireveritas4’ reads the same backwards as forwards.</li>

</ol>

<h2>Marking Guide (total 3.5 marks)</h2>

Marks are given for the correct behavior of the different functions:

<ul>

 <li>1 mark for decode.</li>

 <li>1 mark for pattern count.</li>

 <li>5 marks if palindrome can correctly identify that a string with no processing is a palindrome (see Examples a and b), 1.5 marks if palindrome can correctly identify that a string when converted to lower case alphanumeric characters is a palindrome (see Examples c, d, and e).</li>

</ul>

<h1>Task 2: Friends (4.5 Marks)</h1>

You have been employed by Monash to analyse friendship groups on campus. Individuals have been allocated a number between 0 and the number of people on campus (minus one), and their friendships have been recorded as edges between numbered vertices. We assume friendships are always bi-directional. Monash has implemented this graph in a Python-readable format as both an adjacency matrix and an adjacency list.

Create a Python module called friends.py. Within this module implement the following three tasks. Ensure you follow the inputs for each function correctly – one function takes an adjacency list, two functions take an adjacency matrix. You may not import any other libraries or modules.

<h2>Part A: Popular (1.5 Marks)</h2>

Write a function popular(graph list, n) that returns a list of people who have at least n friends. Each person is identified by the number of their vertex.

<strong>Input</strong>: a nested list graph list that represents a graph as an adjacency list, that models the friendships at Monash; and a non-negative integer n.

<strong>Output</strong>: a list of integers, where each integer is a person with at least n friends. If no person has at least n friends, return an empty list. The list may be in any order.

<strong>Examples </strong>clayton_list = [ [1,2,3], [0,3], [0,4], [0,1], [2] ]

The example graph clayton list is provided for illustrative purpose. Your implemented function must be able to handle arbitrary graphs in <strong>list </strong>form.

<ol>

 <li>Calling popular(clayton list,2) returns [0,1,2,3].</li>

 <li>Calling popular(clayton list,3) returns [0].</li>

 <li>Calling popular(clayton list,0) returns [0,1,2,3,4].</li>

</ol>

<h2>Part B: Friend of a Friend (1.5 Marks)</h2>

Write a function foaf(graph matrix, person1, person2) that determines whether two people have exactly one degree of separation: that is, whether two (distinct)<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> people are not friends, but have at least one friend in common.

<strong>Input</strong>: a nested list graph matrix that represents a graph as an adjacency matrix, that models the friendships at Monash; an integer person1, and an integer person2, where 0 ≤person1, person2<em>&lt; </em>number of people on campus, and person16= person2.

<strong>Output</strong>: a boolean, True if the two people are not friends and they have at least one friend in common; otherwise False.

<h3>Examples</h3>

clayton_matrix = [ [0,1,1,1,0],

[1,0,0,1,0],

[1,0,0,0,1],

[1,1,0,0,0],

[0,0,1,0,0] ]

The example graph clayton matrix is provided for illustrative purpose. Your implemented function must be able to handle arbitrary graphs in <strong>matrix </strong>form.

<ol start="2">

 <li>Calling foaf(clayton matrix,0,4) returns True as 0 and 4 are both friends with 2.</li>

 <li>Calling foaf(clayton matrix,0,3) returns False as 0 and 3 are friends directly.</li>

 <li>Calling foaf(clayton matrix,1,4) returns False as 1 and 4 have no friends in common.</li>

</ol>

<h2>Part C: Society (1.5 Marks)</h2>

Write a function society(graph matrix, person) that determines whether a person has two friends who are also friends with each other.

<strong>Input</strong>: a nested list graph matrix that represents a graph as an adjacency matrix, that models the friendships at Monash; and an integer person, where 0 ≤person<em>&lt; </em>number of people on campus.

<strong>Output</strong>: a boolean, True if person has at least two friends who are also friends with each other; otherwise False.

<h3>Examples</h3>

<ol>

 <li>Calling society(clayton matrix,0) returns True as 1 and 3 are both friends with 0.</li>

 <li>Calling society(clayton matrix,2) returns False as 2 is friends with 0 and 4, but 0 and 4 are not friends with each other.</li>

</ol>

<h2>Marking Guide (total 4.5 marks)</h2>

Marks are given for the correct behavior of the different functions:

<ul>

 <li>5 marks for popular.</li>

 <li>5 marks for foaf.</li>

 <li>5 marks for society.</li>

</ul>

<h1>Task 3: Cards (4 Marks)</h1>

A friend of yours is developing a prototype for a website on which people can play poker. They have contacted you to help them implement some of the project’s backend: specifically, they would like some help telling what kind of hand a player has played. You have agreed to implement four functions to assist them.

In the backend, your friend has decided to represent cards as tuples comprising an integer and a string: (rank, suit). For example, the seven of clubs would be represented as (7, ‘C’). As this is a prototype, your friend has told you that no face cards will be used (that is, rank is always an integer, where 2 ≤ rank ≤ 10, unless otherwise specified). There are four suits, with the following string representations: clubs: ‘C’, diamonds: ‘D’, hearts: ‘H’, spades: ‘S’. As this is poker, which is only played with one deck of cards, there will never be duplicates, and each hand will contain exactly five cards.

Create a Python module called cards.py. Within this module implement the following four tasks. For this module you may <strong>not </strong>use the Python inbuilt function sorted() or the Python method list.sort(). You may not import any other libraries or modules.

<h2>Part A: Suits (1 Mark)</h2>

Write a function suits(hand) that sorts a given hand into the four suits. As there is no standard ranking of suits in poker, we will order alphabetically: clubs, diamonds, hearts, spades.

<strong>Input</strong>: a list hand containing five cards.

<strong>Output</strong>: a nested list containing four lists of cards, with each internal list corresponding to a suit. If there are no cards of that suit in the hand, the internal list for that suit is empty. Cards may be in any order within their suit-list.

<h2>Part B: Flush (1 Mark)</h2>

Write a function flush(hand) that determines whether a given hand is a flush. In poker, a flush is a hand that contains five cards of the same suit.

<strong>Input</strong>: a list hand containing five cards.

<strong>Output</strong>: a boolean, True if all five cards in hand are the same suit, False if not.

<h2>Part C: Straight (2 Marks)</h2>

Write a function straight(hand) that determines whether a given hand is a straight. In poker, a straight is a hand that contains five cards of sequential rank. The cards may be of different suits.

Your friend has asked you an additional favour: they would like to use this function in various other games they may implement in the future, so instead of checking for a five-card straight, they would like you to check for an <em>n </em>card straight, where <em>n </em>is the number of cards in the hand. Like in poker, the cards may be of different suits.

<strong>Input</strong>: a list hand containing at least three cards, where each card may have a rank of some number greater than zero.

<strong>Output</strong>: a boolean, True if the ranks of the cards in hand may be ordered into an unbroken sequence with no rank duplicated, False if not.

<h2>Examples</h2>

<ol>

 <li>Calling suits([(4,‘C’),(8,‘H’),(3,‘C’),(2,‘D’),(8,‘C’)]) returns [[(4,‘C’),(3,‘C’),(8,‘C’)], [(2,‘D’)], [(8,‘H’)], []]. As there are multiple clubs, the clubs cards may be in any order within their internal list.</li>

 <li>Calling flush([(4,‘D’),(8,‘D’),(3,‘D’),(2,‘D’),(10,‘D’)]) returns True.</li>

 <li>Calling flush([(4,‘C’),(8,‘H’),(3,‘C’),(2,‘D’),(8,‘C’)]) returns False.</li>

 <li>Calling straight([(4,‘C’),(2,‘D’),(5,‘S’),(6,‘H’),(3,‘D’)]) returns True.</li>

 <li>Calling straight([(2,‘C’),(3,‘D’),(4,‘S’),(5,‘H’),(5,‘D’)]) returns False.</li>

 <li>Calling straight([(2,‘C’),(3,‘D’),(4,‘S’),(5,‘H’),(7,‘D’)]) returns False.</li>

 <li>Calling straight([(12,‘C’),(13,‘D’),(11,‘D’)]) returns True as the ranks of the cards form an unbroken sequence, [11,12,13], with no rank duplicated.</li>

</ol>

<h2>Marking Guide (total 4 marks)</h2>

Marks are given for the correct behavior of the different functions:

<ul>

 <li>1 mark for suits.</li>

 <li>1 mark for flush.</li>

 <li>1 mark for straight if it is able to handle a normal poker five-card hand with card ranks between 2 and 10 inclusive (see Examples d, e, and f); 2 marks for straight if it is able to handle an arbitrarily large hand with arbitrary ranks (see Example g).</li>

</ul>

<a href="#_ftnref1" name="_ftn1">[1]</a> The functions may return True or False at your discretion for instances where person1 is person2. This case will not be marked.