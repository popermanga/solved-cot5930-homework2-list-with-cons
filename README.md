Download Link: https://assignmentchef.com/product/solved-cot5930-homework2-list-with-cons
<br>
<h1>Problem 1. List with Cons</h1>

Put the required functions in an object called List in file <strong>p1.scala</strong>, in a package called h2.p1. Start with the List code given in class, i.e. the List ADT using the <em>Cons </em>constructor. In the same file add a module called p1 with a <em>main </em>method where you will write part of the solutions.

<ol>

 <li>Write in module p1 a <strong>polymorphic</strong> method called <em>switchHead</em> that takes as argument a list <em>lst </em>and switches the 1<sup>st</sup> and 2<sup>nd</sup> elements from <em>lst</em>. If the list has fewer than two elements throw an exception using function call <em>error</em>(“too short”). Use pattern matching.</li>

</ol>

Example usage:

<strong>val</strong> lst <strong>=</strong> <strong>List</strong>(<strong>0</strong>, <strong>1</strong>, <strong>2</strong>, <strong>3</strong>)

println(<strong>List</strong>.switchHead(lst))    // prints Cons(1,Cons(0,Cons(2,Cons(3,Nil))))   println(<strong>List</strong>.switchHead(<strong>List</strong>(<strong>0</strong>))) // raises java.lang.RuntimeException: too short Write in method p1.main two examples of using this method.

<ol>

 <li>Write in module p1 a <strong>polymorphic</strong> method (with type parameter <em>A</em>) called <em>get</em> that takes as argument a list <em>lst </em>and an integer <em>n</em>. The function returns the element from <em>lst </em>with index <em>n,</em> considering the first element is at index 0. If the index is invalid (&lt;0 or &gt;= size of <em>lst</em>) then <em>get </em>throws an exception using function call <em>error</em>(“wrong index”). Use pattern matching.</li>

</ol>

Example usage:

<strong>val</strong> lst <strong>=</strong> <strong>List</strong>(<strong>0</strong>, <strong>1</strong>, <strong>2</strong>, <strong>3</strong>)

println(<strong>List</strong>.get(lst, <strong>3</strong>))    // prints 3   println(<strong>List</strong>.get(<strong>5</strong>))         // raises java.lang.RuntimeException: wrong index Write in method p1.main two examples of using this method.

<ol>

 <li>Write in module p1 a <strong>polymorphic</strong> method (with type parameter <em>A</em>) called <em>set </em>that takes as argument a list <em>lst, </em>an integer <em>n</em>, and <em>x </em>of type <em>A</em>. The function returns a new list identical to <em>lst </em>except for the element from <em>lst </em>with index <em>n</em> that is replaced by The first list element has index 0. If the given index is invalid (<em>n</em>&lt;0 or &gt;= size of <em>lst</em>) then s<em>et </em>throws an exception using function call <em>sys.error</em>(“wrong index”). Use pattern matching.</li>

</ol>

Example usage:

<strong>val</strong> lst <strong>=</strong> <strong>List</strong>(<strong>0</strong>, <strong>1</strong>, <strong>2</strong>, <strong>3</strong>)

println(<strong>List</strong>.set(lst, <strong>2</strong>, <strong>100</strong>))  // prints Cons(0, Cons(1, Cons(100, Cons(3, Nil)))

Write in method p1.main two examples of using this method.

<ol>

 <li>Write in module p1 a <strong>polymorphic</strong> method (with type parameter <em>A</em>) called <em>take </em>that takes as argument a list <em>lst: List</em>[<em>A</em>] and an integer <em>n</em>. The function returns a new list with the first <em>n</em> elements from <em>lst</em>. If <em>n</em> is invalid (&lt;0 or &gt;= size of <em>lst</em>) then <em>takeN </em>throws an exception using function call <em>error</em>(“wrong index”). Use pattern matching. This function is quite similar to <em>drop</em>.</li>

</ol>

Example usage:

<strong>val</strong> lst <strong>=</strong> <strong>List</strong>(<strong>0</strong>, <strong>1</strong>, <strong>2</strong>, <strong>3</strong>)

println(<strong>List</strong>.takeN(lst, <strong>2</strong>))   // prints Cons(0,Cons(1,Nil)) Write in method p1.main an example of using this method.

<ol>

 <li>Write in module p1 a <strong>polymorphic</strong> method with this signature: <strong>def</strong> mapsq[<strong>A</strong>](lst<strong>:</strong> <strong>List</strong>[<strong>A</strong>])(f<strong>:</strong> <strong>A</strong> =&gt; A) <strong>:</strong> <strong>List</strong>[<strong>A</strong>]</li>

</ol>

<em>mapsq</em> returns a new list where each element <em>x </em>from the original list <em>lst</em> is replaced by expression <em>f</em>(<em>f</em>(<em>x</em>)). Use the <em>map </em>function.

Write in <em>main</em> an expression with <em>mapsq</em> that obtains a list of elements x * 4 for each element x of List(1,2,3,4), i.e. the same list as List(4,8,12,16). Use the _ notation for the  lambda expression.

Write in <em>main</em> an expression with <em>mapsq</em> that obtains a list of elements x + 6 for each element x of List(1,2,3,4), i.e. the same list as List(7,8,9,10). Use the _ notation for the lambda expression.

<h1>Problem 2. Using the standard library List (::)</h1>

Put the required functions in an object called List in file <strong>p2.scala</strong>, in a package called h2.p2. Use the <strong><em>scala.collection.immutable.List</em></strong> class and <strong>not </strong>the List class detailed in the course. Hence, your solutions must rely on the <strong>::</strong> constructor to stand for <em>Cons, </em>if necessary. In the same file add a module called <em>p2</em> with a <em>main </em>method where you will write part of the solutions.

<ol start="2">

 <li>Write in method <em>main </em>a statement that uses <em>List.foldRight</em> to print the sum of all <strong>odd</strong> numbers from List(13, -1, 0, 2).</li>

 <li>Write in module <em>p2</em> a <strong>polymorphic</strong> method function called <em>toStrings</em> that takes a parameter <em>lst </em>of type List[A] and returns a List[String] where each element <em>x</em> of <em>lst</em> is replaced by <em>toString</em>. Use the <em>map </em>method. Example usage:</li>

</ol>

<strong>val</strong> numbers <strong>=</strong> <strong>List</strong>(<strong>13</strong>, –<strong>1</strong>, <strong>0</strong>, <strong>2</strong>)

println(toStrings(numbers))   // prints List(13, -1, 0, 2), a list of String

Write in method <em>p2.main </em>an example of using this method with Double, different from the previous one.

<ol>

 <li>Write in module <em>p2</em> a <strong>polymorphic</strong> method function called <em>compute</em> <strong>using foldLeft</strong>, that takes in the first parameter list a List[A], in the second parameter list a binary operator <em>f</em> of type (A, A) =&gt; A, and that applies <em>f</em> to all elements of this sequence, going left to right.</li>

</ol>

So, <em>compute</em>(List(a, b, c, d))(f) == f( f( f( a, b), c) , d)

Example usage:

<strong>val</strong> numbers <strong>=</strong> <strong>List</strong>(<strong>13</strong>, –<strong>1</strong>, <strong>0</strong>, <strong>2</strong>)

println(compute(numbers)(<strong>_</strong> + <strong>_</strong>))   // prints 14

<strong>Hint</strong>: The standard List trait has methods <em>head </em>and <em>tail </em>that work as expected.

Write in method <em>p2.main </em>an example of using this method different from the previous one.

<ol>

 <li>Write in module <em>p2</em> a monomorphic method with this signature: <strong>def</strong> splitSum(lst<strong>:</strong> <strong>List</strong>[<strong>Int</strong>])(p<strong>:</strong> <strong>Int</strong> =&gt; <strong>Boolean</strong>) <strong>:</strong> (<strong>Int</strong>, <strong>Int</strong>)</li>

</ol>

<em>splitSum </em>has two parameter lists to assist with type inference. It returns a tuple where the first element is the sum of all elements <em>x</em> from <em>lst </em>for which <em>p</em>(<em>x</em>) is true and the second element is the sum of all elements <em>x</em> from <em>lst </em>where for which <em>p</em>(<em>x</em>) is not true, i.e. expression (∑<em><sub>x</sub></em><sub>∈<em>lst</em>∧<em>p</em>(<em>x</em>) </sub><em>x ,</em>∑<em><sub>x</sub></em><sub>∈<em>lst</em>∧<em>!p</em>(<em>x</em>) </sub><em>x</em>) Write in method <em>p2.main </em>an example on a List[Int] that prints the tuple with the sum of even numbers and the sum of odd numbers from that list.

<ol>

 <li><strong>Extra credit: 3 points</strong></li>

</ol>

Write in module p2 a <strong>polymorphic</strong> method with this signature: <strong>    def</strong> split[<strong>A</strong>](xs<strong>:</strong> <strong>List</strong>[<strong>A</strong>])(p<strong>:</strong> <strong>A</strong> =&gt; <strong>Boolean</strong>) <strong>:</strong> (<strong>List</strong>[<strong>A</strong>], <strong>List</strong>[<strong>A</strong>])

that returns a partition of list <em>xs</em> based on predicate <em>p</em>: the first element of the returned tuple is a list with elements <em>x</em> from <em>xs</em> where p(x) is true and the second element of the returned tuple is a list with elements <em>x</em> from <em>xs</em> where p(x) is false. The order of elements in these lists must be preserved. Use one of the <em>fold </em>methods.

Example usage:

<strong>val</strong> lst <strong>=</strong> <strong>List</strong>(<strong>0</strong>, <strong>1</strong>, <strong>2</strong>, <strong>3</strong>)

println(split(lst)(<strong>_</strong> &lt; <strong>2</strong>))     // prints (List(0, 1), List(2, 3))

Write in method <em>p2.main </em>an example of using this method different from the previous one.




<ol>

 <li><strong>Extra credit: 3 points</strong></li>

</ol>

Write in module p2 a <strong>polymorphic</strong> method with this signature: <strong>  def filterFoldRight</strong><strong>[</strong><strong>A</strong><strong>, </strong><strong>B</strong><strong>](</strong><strong>xs: </strong><strong>List</strong><strong>[</strong><strong>A</strong><strong>],</strong><strong> z: </strong><strong>B</strong><strong>)(</strong><strong>p: </strong><strong>A</strong> <strong>=&gt;</strong> <strong>Boolean</strong><strong>)(</strong><strong>f: </strong><strong>(</strong><strong>A</strong><strong>,</strong> <strong>B</strong><strong>)</strong><strong> =&gt; B</strong><strong>)</strong><strong> : </strong><strong>B</strong>

using <em>pattern matching</em> that applies the binary operator <em>f</em> in a right-to-left order only to elements <em>x </em>of list <em>xs </em>for which <em>p</em>(<em>x</em>) is true.

Write a second version called <em>filterFoldRight_1</em> that does the same thing using the <em>foldRight</em> function.

Write in method <em>p2.main </em>an example of using each of this function.

<h1>Problem 3. Tree</h1>

Put the required functions in an object called List in file <strong>p3.scala</strong>, in a package called h2.p3. Start with the <em>Tree </em>ADT code from the textbook. In the same file add a module called <em>p3</em> with a <em>main </em>method where you will write part of the solutions.

<ol start="3">

 <li>Write an expression in method <em>main</em> that computes the product of all leaves in a tree of <em>Int</em>s using the <em>Tree.fold </em>method. If Scala type inference produces unreasonable compilation errors just don’t use _ (underscore) for your lambda expressions.</li>

 <li>Consider this tree variable: <strong>val</strong> tree<strong>:</strong> <strong>Tree</strong>[<strong>Int</strong>] <strong>=</strong> <strong>Branch</strong>(<strong>Branch</strong>(<strong>Leaf</strong>(<strong>2</strong>), <strong>Leaf</strong>(<strong>3</strong>)), <strong>Branch</strong>(<strong>Leaf</strong>(<strong>4</strong>), <strong>Leaf</strong>(<strong>5</strong>)))</li>

</ol>

Write an expression in method <em>p3.main</em> with the <em>Tree.map </em>function that computes the tree with the same structure of variable <em>tree</em> but with each leaf value being formatted to a string. The result must be the same as the following Tree[String] :

<strong>Branch</strong>(<strong>Branch</strong>(<strong>Leaf</strong>(“leaf 2”),<strong>Leaf</strong>(“leaf 3”)),<strong>Branch</strong>(<strong>Leaf</strong>(“leaf 4”),<strong>Leaf</strong>(“leaf 5”)))

<ol start="3">

 <li>Write in module Tree (file p3.scala) a <strong>polymorphic</strong> method with this signature: <strong>def</strong> toList[<strong>A</strong>](t<strong>:</strong> <strong>Tree</strong>[<strong>A</strong>]) <strong>:</strong> <strong>List</strong>[<strong>A</strong>]</li>

</ol>

that returns a list (i.e. standard library List) with all elements from the leaves in tree <em>t</em>. Use the <em>Tree.fold </em>method given from the textbook.

<em>Hint</em>: the List.++ method appends two lists.

Example usage:

<strong>val</strong> tree<strong>:</strong> <strong>Tree</strong>[<strong>Int</strong>] <strong>=</strong> <strong>Branch</strong>(<strong>Branch</strong>(<strong>Leaf</strong>(<strong>2</strong>), <strong>Leaf</strong>(<strong>3</strong>)), <strong>Branch</strong>(<strong>Leaf</strong>(<strong>4</strong>), <strong>Leaf</strong>(<strong>5</strong>)))    println(<strong>Tree</strong>.toList(tree))   // prints List(2, 3, 4, 5)

Write in method <em>p3.main </em>an example of using this method different from the previous one.

<h1>Problem 4. Option/Either</h1>

Write the solution in a file <strong>p4.scala</strong>, in a package called h2.p4. Use (or import) the Option and Either code given in the course. In the same file add a module called <em>p4</em> with a <em>main </em>method where you will write part of the solutions.

<ol>

 <li>a) Unit testing is vital for building robust code. Write in module <em>p4</em> a simple unit test function that has this signature:</li>

</ol>

<strong>   def</strong> testFunction2[<strong>A</strong>,<strong>B</strong>,<strong>C</strong>](testname<strong>:</strong> <strong>String</strong>, a<strong>:</strong> <strong>A</strong>, b<strong>:</strong> <strong>B</strong>, expected<strong>:</strong> <strong>C</strong>)(f<strong>:</strong> (<strong>A</strong>,<strong>B</strong>) <strong>=&gt;</strong> C)         <strong>:</strong> <strong>Either</strong>[<strong>String</strong>, <strong>String</strong>]

This function returns <strong>Right</strong>(testname + ” passed”) if f(a,b) == expected and <strong>Left</strong>(testname + ” failed”) otherwise. Using the <em>Either</em> ADT allows the programmer to quickly separate failed vs. passed tests, e.g. using pattern matching.

The purpose of this function is to automate testing for functions with two arguments, as in the next example:

<strong>def</strong> sample_add(x<strong>:</strong> <strong>Int</strong>, y<strong>:</strong> <strong>Int</strong>)<strong>:</strong> <strong>Int</strong> = x + y    // function we want to test

// we set up a “test vector” with values 10, 20, 30, where 30 is the expected return value:

<strong>val</strong> add_test_result <strong>=</strong> testFunction2(“sample_add”, <strong>10</strong>, <strong>20</strong>, <strong>10</strong> + <strong>20</strong>)(sample_add)  println(add_test_result)     // a Right value means the test passed: prints Right(sample_add passed)

<ol>

 <li>Write in module p4 a function <em>sumO </em>that takes as arguments <em>x </em>and <em>y </em>(two Option[Int] objects) and returns the sum of the values in <em>x</em> and <em>y</em> in a Some constructor or <em>None</em>, if at least one of <em>x </em>and <em>y </em>is <em>None</em>. Use the <em>map2 </em>function to get credit.</li>

</ol>

Write a new version of this function called <em>sumO_1</em> using <em>flatMap </em>and <em>map, </em>to get credit.

Write a new version of this function called <em>sumO_2</em> using a <em>for comprehension, </em>to get credit.

Write code in <em>p4.main</em> that uses the <em>testFunction2</em> function to test <em>sumO</em>,  <em>sumO_1</em>,  and <em>sumO_2. </em>At least one of the tests must use a <em>None </em>value for parameter <em>a</em> or parameter <em>b</em>.

<ol>

 <li>Consider the <em>lift</em> function given in the textbook that converts an A =&gt; B function into an Option[A] =&gt; Option[B] function. Write in module p4 a function called <em>lift2</em> that converts an (A,B)=&gt;C function into an (Option[A], Option[B]) =&gt; Option[C] function. Don’t do pattern matching in this function. Instead, use the utility functions from the Option object or a for comprehension.</li>

</ol>

Example usage:

<strong>def</strong> sample_add(x<strong>:</strong> <strong>Int</strong>, y<strong>:</strong> <strong>Int</strong>)<strong>:</strong> <strong>Int</strong> = x + y    // function we want to test

<strong>val</strong> add_lifted <strong>=</strong> lift2(sample_add)   println(add_lifted(<strong>Some</strong>(<strong>10</strong>), <strong>Some</strong>(<strong>20</strong>)))  // prints Some(30)

<h1>Problem 5. Validation with Option/Either</h1>

Write the solution in a file <strong>p5.scala</strong>, in a package called h2.p5. Use (or import) the Option and Either code given in the course. In the same file add a module called <em>p5</em> with a <em>main </em>method where you will write part of the solutions.

Consider the following Student class: <strong>  sealed</strong> <strong>case</strong> <strong>class</strong> <strong>Student</strong>(name<strong>:</strong> <strong>String</strong>, id<strong>:</strong> <strong>Int</strong>, grades<strong>:</strong> <strong>List</strong>[<strong>Double</strong>])

Write a function called <em>mkStudent</em> that parses those Strings parameters and produces a new Student class as a <em>Right </em>value if input parsing is successful or a <em>Left</em>(<em>exception</em>) if <em>name</em> is an empty or string parsing failed for <em>id</em> or any of the strings in the <em>grades</em> list. Use a <strong>for comprehension</strong>. The function’s signature is:

<strong>  def</strong> mkStudent(name<strong>:</strong> <strong>String</strong>, idstr<strong>:</strong> <strong>String</strong>, gradesstr<strong>:</strong> <strong>List</strong>[<strong>String</strong>])<strong>:</strong> <strong>Either</strong>[<strong>Exception</strong>, <strong>Student</strong>]

Example usage with a <em>Right </em>value:

<strong>val</strong> studentE <strong>=</strong> mkStudent(“Jane”, “1234”, <strong>List</strong>(“90.0”, “95”, “73”, “78”))  println(studentE)

// prints Right(Student(Jane,1234,List(90.0, 95.0, 73.0, 78.0)))

Example usage with a <em>Left </em>value, when parsing failed:

<strong>val</strong> studentF <strong>=</strong> mkStudent(“Jose”, “5678”, <strong>List</strong>(“90.0”, “X95”, “73”, “78”))

// prints Left(java.lang.NumberFormatException: For input string: “X95”)      println(studentF)

Write in <em>p5.main</em> different 2 examples with <em>mkStudent</em> that produce (and print) a <em>Right</em> value and a <em>Left </em>value.