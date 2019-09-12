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
left a mess to be cleared up later.<!-- .element: class="fragment" data-fragment-index="1" -->

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



Code which is coupled is tedious to refactor.

Code which's behaviour is not described is hard to enhance without regression erros.<!-- .element: class="fragment" data-fragment-index="1" -->

Code which is not described by tests let's you hardly identify unused or not required parts.<!-- .element: class="fragment" data-fragment-index="2" -->

Production code which already exists and which is supposedly working is boring to characterize!<!-- .element: class="fragment" data-fragment-index="3" -->



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



### SOLID

<ul>
    <li class="fragment" data-fragment-index="1"><span style="color:orange">S</span>ingle Responsibility Principle</li>
    <li class="fragment" data-fragment-index="2"><span style="color:orange">O</span>pen Close Principle</li>
    <li class="fragment" data-fragment-index="3"><span style="color:orange">L</span>iskov Substitution Principle</li>
    <li class="fragment" data-fragment-index="4"><span style="color:orange">I</span>nterface segregation Principle</li>
    <li class="fragment" data-fragment-index="5"><span style="color:orange">D</span>ependency Inversion Principle</li>
</ul>



### Single Responsibility Principle

<blockquote cite="Robert C. Martin">
    A class should have only one reason to change (Robert C. Martin)
</blockquote>



Imagine you have a class Employee like this:

<pre class="java"><code>
public class Employee {
    private Date dateOfJoining;
    // & other Attributes
    // Getters & Setters forattributes

    public boolean isPromotionDue() {
        //Code to determine promotion
    }
        
    public calculateIncomeTax() {
        //Code to calculate tax
    }
}
</code></pre>



### How about seperating concerns?

<pre class="java"><code>
public class HRPromotion {
    public boolean is PromotionDue(Employee employee) {
        // Code to determine promotion
    }
}

public class TaxCalculator {
    public boolean calculateTaxFor(Employee employee) {
        // Code to calculate tax
    }
}
</code></pre>



Which would make your employee class look like this:
<pre class="java"><code>
    public class Employee {
        private Date dateOfJoining;
        // & other Attributes
        // Getters & Setters for attributes
    }
</code></pre>



### Open closed principle

<blockquote cite="Robert C. Martin">
    A class should have only one reason to change (Robert C. Martin)
</blockquote><!-- .element: class="fragment" data-fragment-index="1" -->



Imagine you have following class:

<pre class="java"><code>
public class AreaCalculator {
    public double calculateArea(List&lt;Rectangle&gt rectangles) {
        double area;

        for (Rectangle rectangle : rectangles) {
            area += rectangle.width * rectangle.height;
        }

        return area;
    }
}
</code></pre>



Imagine moreover you'd now have circles.

What would you most likely do?<!-- .element: class="fragment" data-fragment-index="1" -->
<pre class="java"><code>
public class AreaCalculator {
    public double calculateArea(List&lt;Shape&gt shapes) {
        double area;
        
        for (Shape shape : shapes) {
            if (shape.getType() == "Rectangle") {
                area += shape.width * shape.height;
            }

            area += Math.pow(shape.radius, 2) * Math.PI;
        }

        return area;
    }
}
</code></pre><!-- .element: class="fragment" data-fragment-index="2" -->



### So what to do?

Maybe something like this:<!-- .element: class="fragment" data-fragment-index="1" -->
<pre class="java"><code>
public class AreaCalculator {
    public double calculateArea(List&lt;Shape&gt shapes) {
        double area;

        for (Shape shape : shapes) {
            area += shape.calculateArea();
        }

        return area;
    }
}
</code></pre><!-- .element: class="fragment" data-fragment-index="1" -->



Which would leave your Shapes to look like this:
<pre class="java"><code>
public class Circle implements Shape {
    private double radius;

    @Override
    public double calculateArea() {
        return Math.pow(radius, 2) * Math.PI;
    }
}

public class Square implements Shape {
    private double radius;

    @Override
    public double calculateArea() {
        return height * width;
    }
}
</code></pre>



### Liskov Substitution Principle

<blockquote>
   If for each object O1 of type S and an object O2 of type T such that for all program P defined in terms of T, the behavior of P is unchanged when O1 is substituted for O2 then S is a subtype of T. (Barbara Liskov, 1981)
</blockquote><!-- .element: class="fragment" data-fragment-index="1" -->



### The principle defines the behavioral rules of inheritance
<blockquote>
    Instance of desired class must be usable through the interface of its base class without clients of the base class being able to tell the difference. Subtypes must be substitutable for their base types.
</blockquote>



### Interface Segregation

<blockquote>
Clients should not be forced to implement interfaces they don't use.

Instead of one fat interface many small interfaces are preferred based on groups of methods, each one serving one submodule.
</blockquote><!-- .element: class="fragment" data-fragment-index="1" -->



### Dependency Inversion Principle

<blockquote>
High-level modules should not depend on low-level modules. Both should depend on abstractions.<!-- .element: class="fragment" data-fragment-index="1" -->

Abstractions should not depend on details. Details should depend on abstractions.<!-- .element: class="fragment" data-fragment-index="2" -->
</blockquote>



Imagine you'd have an implementation of switch.
<pre class="java"><code>
package de.igel.university;
import com.partner.devices.Lamp;

public class Switch {
    Lamp lamp = new Lamp();

    public void turnOn() {
        lamp.on();
    }

    public void turnOff() {
        lamp.off();
    }
}
</code></pre>



What happens to the switch class if something changes in the lamp class?

So how about:<!-- .element: class="fragment" data-fragment-index="1" -->
<pre class="java"><code>
package de.igel.lamp.switch;

public class Switch {
    public void turnOn(Device device) {
        device.turnOn();
    }

    public void turnOff(Device device) {
        device.turnOff();
    }
}

interface Device {
    void turnOn();

    void turnOff();
}
</code></pre><!-- .element: class="fragment" data-fragment-index="2" -->



Hence it is now easy to implement various devices. Like:
<pre class="java"><code>
package another.companys.weird.lamp;

public class MegaLamp implements Device {
    @Override
    public void turnOn() {
        // implementation
    }

    @Override
    public void turnOff() {
        // implementation
    }
}
</code></pre>