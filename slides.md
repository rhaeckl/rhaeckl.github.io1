### Food for thought!

Who do you want to be?



Every developer is a programmer

but not every programmer is a developer! <!-- .element: class="fragment" data-fragment-index="1" -->

<table><tr>
<td> <img src="rhaeckl.github.io/images/work-933061_640.jpg" alt="Drawing" style="width: 300px;"/> </td>
<td> <img src="rhaeckl.github.io/images/company-concept-creative-7369.jpg" alt="Drawing" style="width: 300px;"/> </td> <!-- .element: class="fragment" data-fragment-index="1" -->
</tr></table>



To be more specific:

<table border="0">
 <tr style="border:0">
    <td style="border:0"><b style="font-size:30px">Programmer</b></td><!-- .element: class="fragment" data-fragment-index="1" -->
    <td style="border:0"><b style="font-size:30px">Developer</b></td><!-- .element: class="fragment" data-fragment-index="2" -->
 </tr>
 <tr style="border:0">
    <td style="border:0"><p style="font-size:30px">is a problem solver</></td><!-- .element: class="fragment" data-fragment-index="1" -->
    <td style="border:0"><p style="font-size:30px">is a formally trained programmer</p></td><!-- .element: class="fragment" data-fragment-index="2" -->
 </tr>
 <tr style="border:0">
    <td style="border:0"><b style="font-size:30px">The Objective</b></td><!-- .element: class="fragment" data-fragment-index="1" -->
    <td style="border:0"><b style="font-size:30px">The Objective</b></td><!-- .element: class="fragment" data-fragment-index="2" -->
 </tr>
 <tr style="border:0">
    <td style="border:0"><p style="font-size:30px">Someone who can solve problems by manipulating code.</p></td><!-- .element: class="fragment" data-fragment-index="1" -->
    <td style="border:0"><p style="font-size:30px">To solve problems or create things in accordance with design and implementation principles, including performance, maintainability, scalability, robustness, readability and security.</p></td><!-- .element: class="fragment" data-fragment-index="2" -->
 </tr>
</table>



### Ask yourself,
### for whom do you write code?
You write code not to show off, but to make things work.<!-- .element: class="fragment" data-fragment-index="1" -->
You write code for your colleagues to read.<!-- .element: class="fragment" data-fragment-index="1" -->



### Do you have to rush?
#### Yes, because
deadline is coming close.<!-- .element: class="fragment" data-fragment-index="1" -->

Backlog is getting bigger and bigger.<!-- .element: class="fragment" data-fragment-index="2" -->

...<!-- .element: class="fragment" data-fragment-index="2" -->



### What did you do?
#### I then
left a mess to be clead up later.<!-- .element: class="fragment" data-fragment-index="1" -->

wrote hacks.<!-- .element: class="fragment" data-fragment-index="2" -->

stayed late.<!-- .element: class="fragment" data-fragment-index="3" -->

...<!-- .element: class="fragment" data-fragment-index="3" -->



### Why do you probably do this?
I am afraid of being fired.<!-- .element: class="fragment" data-fragment-index="1" -->

I am afraid that I will not advance in my company.<!-- .element: class="fragment" data-fragment-index="2" -->

...<!-- .element: class="fragment" data-fragment-index="2" -->



### Think twice!
Your job is to defend your code with equal passion.



### Do not forget
POs and Managers<!-- .element: class="fragment" data-fragment-index="1" -->

need to defend their timeline,<!-- .element: class="fragment" data-fragment-index="2" -->

depend on your expert knowledge<!-- .element: class="fragment" data-fragment-index="3" -->



# TDD
### Test DRIVEN development


### Writing specifications
Describe the behaviour of your units



### What TDD is <span style="color:red">NOT</span>
TDD is not about testing!<!-- .element: class="fragment" data-fragment-index="1" -->

TDD is not a tool to make your code waterproof!<!-- .element: class="fragment" data-fragment-index="2" -->

TDD doesn't prevent you from making errors!<!-- .element: class="fragment" data-fragment-index="3" -->



### So then,
### why would you do TDD?



### Preventing bugs is cheaper than fixing bugs
<img src="rhaeckl.github.io/images/comparingTechniques.jpg" width="500">



### Benefits of TDD?



#### You have to think

about the requirements.<!-- .element: class="fragment" data-fragment-index="1" -->

about the desired behaviour.<!-- .element: class="fragment" data-fragment-index="2" -->



#### You will

ensure quality.<!-- .element: class="fragment" data-fragment-index="1" -->

have more confidence in your code.<!-- .element: class="fragment" data-fragment-index="2" -->

be able to ship in short intervals.<!-- .element: class="fragment" data-fragment-index="3" -->

know that everything worked just couple minutes ago.<!-- .element: class="fragment" data-fragment-index="4" -->



#### You will

do small steps.<!-- .element: class="fragment" data-fragment-index="1" -->

focus on one task.<!-- .element: class="fragment" data-fragment-index="2" -->



#### Your code will

be safer to refactor.<!-- .element: class="fragment" data-fragment-index="1" -->

be de-coupled.<!-- .element: class="fragment" data-fragment-index="2" -->

be moldable instead of rigid.<!-- .element: class="fragment" data-fragment-index="3" -->



# Why not test afterwards?



Code which is copled is tedious to refactor.<!-- .element: class="fragment" data-fragment-index="1" -->

Code which's behaviour is not described is hard to enhance without regression erros.<!-- .element: class="fragment" data-fragment-index="2" -->

Code which is not described by tests let's you hardly identify unused or not required parts.<!-- .element: class="fragment" data-fragment-index="3" -->

Production code which already exists and which is supposedly working is boring to characterize!<!-- .element: class="fragment" data-fragment-index="4" -->



# TDD is an investment!



### Understand that tests

have to be executed<!-- .element: class="fragment" data-fragment-index="1" -->

have to finish fast.<!-- .element: class="fragment" data-fragment-index="2" -->

have to be independent.<!-- .element: class="fragment" data-fragment-index="3" -->

need the same kind of maintenance as production code.<!-- .element: class="fragment" data-fragment-index="4" -->



Let's do a hands on



# How to do TDD?



<img src="rhaeckl.github.io/images/tdd.png" width="500">


#### How to write a Test?

Think about a baby step!<!-- .element: class="fragment" data-fragment-index="1" -->

Always start with an assertion!<!-- .element: class="fragment" data-fragment-index="2" -->

Arrange yourself<!-- .element: class="fragment" data-fragment-index="3" -->

then get your act together!<!-- .element: class="fragment" data-fragment-index="4" -->



<pre class="java"><code>
@Test
public void wrap_whenEmptyWord_thenReturnEmptyWord() {
    // Arrange
    TextWrapper textWrapper = new TextWrapper();
    
    // Act
    String wrappedText = textWrapper.wrap("");

    // Assert
    assertThat(wrappedText).isEqualTo("");
}
</code></pre>



#### Please mind that

the more detailed your tests get<!-- .element: class="fragment" data-fragment-index="1" -->

the more generic your code gets!<!-- .element: class="fragment" data-fragment-index="2" -->