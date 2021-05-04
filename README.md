# Introduction to Probability

## Introduction

Now that you understand the basics of sets, you'll learn how this knowledge can be used to calculate your first probabilities! In this section, you'll learn how to use sets to create probabilities and you'll learn about the foundations of probability through the three probability axioms.

## Objectives

You will be able to: 

* Compare experiments, outcomes, and the event space
* Calculate probabilities by using relative frequency of outcomes to event space
* Describe the three axioms of probability
* Describe the addition law of probability

## Probability Terminology

For the following examples, we will consider what happens when throwing a single 6-sided die ("die" is the singular of ["dice"](https://en.wikipedia.org/wiki/Dice)).

### Experiments and Outcomes

When you throw a die once, you can consider this a ***random experiment***. The result of this "experiment" is the ***outcome***. So, for example, the outcome could be a 2. 

### Events

An ***event*** is the outcome of a particular random experiment. So, for example, "rolling the die and getting a 5" is an event.

### Sample Spaces

The ***sample space*** represents the universe of all possible outcomes. With our die rolling example, that space includes the values of 1, 2, 3, 4, 5, and 6.

### Event Spaces

The ***event space*** is a subset of the sample space. You can think of it as the collection of events we "care about" out of all possible events. For example, our event space could be "rolling a number higher than a 4", which would include the values of 5 and 6.

## Sets and Probability

As you may have noticed, we used the term "subset" to describe event spaces. Sets are a very useful way to represent the probability concepts described above. Let's expand on that now.

### Sample Spaces as Sets

Let's define the sample space for rolling a single die as the set  <img src="https://render.githubusercontent.com/render/math?math=S"> .  <img src="https://render.githubusercontent.com/render/math?math=S"> looks like this:

 <img src="https://render.githubusercontent.com/render/math?math=S= \{1,2,3,4,5,6\}"> 

You can then say that:

-  <img src="https://render.githubusercontent.com/render/math?math=S"> defines all the possible outcomes when throwing the die once
-  <img src="https://render.githubusercontent.com/render/math?math=S"> is our universal set  <img src="https://render.githubusercontent.com/render/math?math=\Omega"> , as seen before

Other examples of sample spaces:

#### The number of text messages you send each day:
- In this case,  <img src="https://render.githubusercontent.com/render/math?math=S"> is equal to some number x, with x being a **non-negative integer**
- Mathematically, x being an integer looks like  <img src="https://render.githubusercontent.com/render/math?math=x \in \mathbb{Z}"> .  <img src="https://render.githubusercontent.com/render/math?math=\mathbb{Z}"> is a "special" set, containing all integers.
- x being non-negative looks like  <img src="https://render.githubusercontent.com/render/math?math=x \geq 0"> 
- To represent the set of x values that meet both requirements, we'll use an additional way of defining a set, called the "set builder" notation. In set builder notation, the vertical bar  <img src="https://render.githubusercontent.com/render/math?math=\mid"> means "such that", and the conditions are separated by commas
- Our overall definition of  <img src="https://render.githubusercontent.com/render/math?math=S"> is  <img src="https://render.githubusercontent.com/render/math?math=S = \{x \mid x \in \mathbb{Z}, x \geq 0\}"> . In other words,  <img src="https://render.githubusercontent.com/render/math?math=S"> contains all instances of x such that x is an integer and x is greater than and equal to zero.

#### The number of hours someone watches TV each day:
- In this case, let's say that x is a **real number between 0 and 24**
- Mathematically, x being a real number (roughly equivalent to a floating point value, although there are subtle differences) looks like  <img src="https://render.githubusercontent.com/render/math?math=x \in \mathbb{R}"> .  <img src="https://render.githubusercontent.com/render/math?math=\mathbb{R}"> is another special set, the set of all real numbers.
- x being between 0 and 24 looks like  <img src="https://render.githubusercontent.com/render/math?math=0 \leq x \leq 24"> 
- Putting that all together, we get  <img src="https://render.githubusercontent.com/render/math?math=S = \{x \mid x \in \mathbb{R}, 0 \leq x \leq 24 \}"> . In other words,  <img src="https://render.githubusercontent.com/render/math?math=S"> contains all instances of x such that x is a real number and x is between 0 and 24.

### Event Spaces as Sets

Let's define the event space as  <img src="https://render.githubusercontent.com/render/math?math=E"> . As noted previously,  <img src="https://render.githubusercontent.com/render/math?math=E  \subseteq S"> , i.e.  <img src="https://render.githubusercontent.com/render/math?math=E"> is a subset of  <img src="https://render.githubusercontent.com/render/math?math=S"> .

An example of  <img src="https://render.githubusercontent.com/render/math?math=E"> could be "rolling a number higher than 4". This would be written  <img src="https://render.githubusercontent.com/render/math?math=E=\{5, 6\}"> .

Or if  <img src="https://render.githubusercontent.com/render/math?math=E"> were "rolling an odd number", that would be written  <img src="https://render.githubusercontent.com/render/math?math=E= \{1,3,5\}"> .

Once  <img src="https://render.githubusercontent.com/render/math?math=E"> is defined, we can say that event  <img src="https://render.githubusercontent.com/render/math?math=E"> happened if the actual outcome after rolling the die belongs to the predefined event space  <img src="https://render.githubusercontent.com/render/math?math=E"> .

Other examples of event spaces based on previously defined sample spaces:

#### Low daily number of text messages sent:
- We can define this as 20 or fewer text messages
- The event space still includes only non-negative integers, but this time there is an upper bound of 20 also
-  <img src="https://render.githubusercontent.com/render/math?math=E = \{x \mid x \in \mathbb{Z}, 0 \leq x \leq 20 \}"> . In other words,  <img src="https://render.githubusercontent.com/render/math?math=S"> contains all instances of x such that x is an integer between 0 and 20.

#### Binge-watch day:
- We can define this as 6 or more hours watched
- The event space still includes only real numbers below 24, but now the lower bound is 6 rather than 0
-  <img src="https://render.githubusercontent.com/render/math?math=E = \{x \mid x \in \mathbb{R}, 6 \leq x \leq 24 \}"> . In other words,  <img src="https://render.githubusercontent.com/render/math?math=S"> contains all instances of x such that x is a real number between 6 and 24.

## Introduction to Probability

Once you understand sample spaces and event spaces, you understand the foundational concepts of probability.

### The Law of Relative Frequency

While conducting an endless stream of experiments, the relative frequency by which an event will happen becomes a fixed number. 

Let's denote an event by  <img src="https://render.githubusercontent.com/render/math?math=E"> , and the _probability_ of the event  <img src="https://render.githubusercontent.com/render/math?math=E"> occurring by  <img src="https://render.githubusercontent.com/render/math?math=P(E)"> . Next, let  <img src="https://render.githubusercontent.com/render/math?math=n"> be the number of conducted experiments, and  <img src="https://render.githubusercontent.com/render/math?math=S(n)"> the count of "successful" experiments (i.e. the times that event  <img src="https://render.githubusercontent.com/render/math?math=E"> happened). The formal definition of probability as a relative frequency is given by:

 <img src="https://render.githubusercontent.com/render/math?math=P(E) = \lim_{n\rightarrow\infty} \dfrac{S{(n)}}{n}"> 

In other words, the probability of the event ( <img src="https://render.githubusercontent.com/render/math?math=P(E)"> ) equals the limit as the number of experiments  <img src="https://render.githubusercontent.com/render/math?math=n"> goes to infinity of the count of successful experiments  <img src="https://render.githubusercontent.com/render/math?math=S(n)"> divided by the number of experiments  <img src="https://render.githubusercontent.com/render/math?math=n"> .

This is the basis of a frequentist statistical interpretation: an event's probability is the ratio of the positive trials to the total number of trials as we repeat the process infinitely. 

###  Probability Axioms

In the early 20th century, Kolmogorov and Von Mises came up with three axioms that further expand on the idea of probability. The three axioms are:

#### 1. Positivity

A probability is always bigger than or equal to 0, or  <img src="https://render.githubusercontent.com/render/math?math=0 \leq P(E) \leq 1"> 

#### 2. Probability of a Certain Event

If the event of interest is the sample space ( <img src="https://render.githubusercontent.com/render/math?math=S = E"> ), we say that the outcome is a certain event, or  <img src="https://render.githubusercontent.com/render/math?math=P(S) = 1"> 

#### 3. Additivity 

The probability of the union of two exclusive events is equal to the sum of the probabilities of the individual events happening.

Remember the inclusion-exclusion principle states that:

 <img src="https://render.githubusercontent.com/render/math?math=\mid S  \cup T\mid = \mid S \mid %2b \mid T \mid - \mid S  \cap T \mid "> 

If we know that  <img src="https://render.githubusercontent.com/render/math?math=S  \cap T = \emptyset"> (that there is no intersection between  <img src="https://render.githubusercontent.com/render/math?math=S"> and  <img src="https://render.githubusercontent.com/render/math?math=T"> , so the set formed by their intersection is the empty set  <img src="https://render.githubusercontent.com/render/math?math=\emptyset"> ), then we can skip that part of the formula, so the cardinality of  <img src="https://render.githubusercontent.com/render/math?math=S  \cup T"> is simply:

 <img src="https://render.githubusercontent.com/render/math?math=\mid S \mid %2b \mid T \mid"> 

The same logic works for the probability of events in two event space sets. If the events are exclusive — they never happen at the same time, so the intersection between them is empty — you can simply add the two probabilities together.

If  <img src="https://render.githubusercontent.com/render/math?math=A  \cap B = \emptyset "> , then  <img src="https://render.githubusercontent.com/render/math?math=P(A \cup B) = P(A) %2b P(B)"> 

### Addition Law of Probability

The additivity axiom is great, but most of the time events are not exclusive. Then we need to bring in the rest of the inclusion-exclusion principle (subtracting the intersection), which is now referred to as the **addition law of probability** or the **sum rule** when we are talking about probabilities.

 <img src="https://render.githubusercontent.com/render/math?math=P(A \cup B) = P(A) %2b P(B) - P(A  \cap B) "> 

Put in words, the probability that  <img src="https://render.githubusercontent.com/render/math?math=A"> or  <img src="https://render.githubusercontent.com/render/math?math=B"> will happen is the sum of the probabilities that  <img src="https://render.githubusercontent.com/render/math?math=A"> will happen and that  <img src="https://render.githubusercontent.com/render/math?math=B"> will happen, minus the probability that *both*  <img src="https://render.githubusercontent.com/render/math?math=A"> and  <img src="https://render.githubusercontent.com/render/math?math=B"> will happen.

## Examples

Let's reconsider the dice example to explain what was explained before:

### Additivity of Exclusive Events

Let's consider two events: event  <img src="https://render.githubusercontent.com/render/math?math=M"> means throwing a 6, event  <img src="https://render.githubusercontent.com/render/math?math=N"> means that you throw an odd number ( <img src="https://render.githubusercontent.com/render/math?math=N={1,3,5}"> ). These events are exclusive, so you can use the additivity rule if you want to know the answer to the question: 

_"what is the probability that your outcome will be a 6, or an odd number?"_

 <img src="https://render.githubusercontent.com/render/math?math=P(M \cup N) = P(M) %2b P(N) = \dfrac{1}{6}%2b\dfrac{3}{6}=\dfrac{4}{6}=\dfrac{2}{3}"> 

There is a 2/3 probability that the outcome will be a 6 or an odd number.

### Addition Law of Probability

Now, let's consider the same event  <img src="https://render.githubusercontent.com/render/math?math=N={1,3,5}"> and another event  <img src="https://render.githubusercontent.com/render/math?math=Q={4,5,6}"> . These events are *not* mutually exclusive, so if you want to know the probability that  <img src="https://render.githubusercontent.com/render/math?math=N"> or  <img src="https://render.githubusercontent.com/render/math?math=Q"> will happen, you need to use the addition law of probability.

Note that  <img src="https://render.githubusercontent.com/render/math?math=(N  \cap Q)"> is equal to getting an outcome of 5, as that is the "common" element in the respective event spaces of  <img src="https://render.githubusercontent.com/render/math?math=N"> and  <img src="https://render.githubusercontent.com/render/math?math=Q"> . This means that  <img src="https://render.githubusercontent.com/render/math?math=P(N  \cap Q) = \dfrac{1}{6}"> 

 <img src="https://render.githubusercontent.com/render/math?math=P(N \cup Q) = P(N) %2b P(Q) - P(N  \cap Q) = \dfrac{3}{6} %2b \dfrac{3}{6} - \dfrac{1}{6} = \dfrac{5}{6} "> 

There is a 5/6 probablity that the outcome will be in  <img src="https://render.githubusercontent.com/render/math?math=N"> or  <img src="https://render.githubusercontent.com/render/math?math=Q"> .


## Final Note

In the previous examples, you noticed that for our dice example, it is easy to use these fairly straightforward probability formulas to calculate probabilities of certain outcomes. 

However, if you think about our text message example, things are less straightforward, e.g.:

_"What is the probability of sending less than 20 text messages in a day?"_

This is where the probability concepts introduced here fall short. The probability of throwing any number between 1 and 6 with a die is always exactly  <img src="https://render.githubusercontent.com/render/math?math=\dfrac{1}{6}"> ,  but we can't simply count our messages event space. In words, the probability of sending 20 messages is likely different than the probability of sending, say, 5 messages, and will be different for any number of messages sent. You'll learn about tools to solve problems like these later on.


## Summary

Well done! In this section, you learned how to use sets to get to probabilities. You learned about experiments, event spaces, and outcomes. Next, you learned about the law of relative frequency and how it can be used to calculate probabilities, along with the three probability axioms.
