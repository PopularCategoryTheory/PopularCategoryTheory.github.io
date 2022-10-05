---
title: "🌱 Introduction to Categories"
mathjax: true
layout: post
---

Hello! 👋

Welcome to my Category Theory blog! I'm so glad you have decided to start exploring Category Theory!

Before you start reading this post, please take a minute to read [about this blog,](https://popularcategorytheory.github.io/aboutblog/) so you know how to use it!

# ❓ What is a Category?

It's the first day of school. Your teacher places a pile of notebooks and textbooks on your desk, and you have no idea what to do with them. You wince as you think about carrying them all back home. You don't even know what you're going to use all of them for.




Your teacher is smart enough to make sense of the horror. She writes the following on the board:

**There are 10 textbooks (one for each subject), and 10 notebooks. Each textbook corresponds to a notebook, and each notebook, corresponds to a textbook.**

You realise you can "pair up" the notebooks and textbooks in a sense. For each subject, you would have one textbook, and one notebook. 

Whether you are consciously aware of it or not, your mind is making this distinction:

![Subjects, Textbooks, Notebooks](https://cdn.discordapp.com/attachments/852828705364770826/1027249426374348860/Screen_Shot_2022-10-05_at_9.31.51_PM.png)

You arrange your textbooks and notebooks accordingly, following instructions.

The next morning, you have mathematics class during the first period. You take out your mathematics textbook, and the notebook you assigned to that textbook (so, your math notebook).

But why are you taking our your mathematics textbook and your mathematics notebook? Why not your physics notebook instead of your math notebook? 

That's because in your mind, the physics notebook does not belong in the same "box" as mathematics. 

A few weeks later, your bus reaches school late. You have no idea which class you just waltzed into. You notice everyone has their physics textbooks on their tables. You're a bit flustered and embarrassed since you got to school late, so you aren't sure which notebook to take out of your bag. The only information you have is that you need your physics textbook, and the notebook should "correspond" to the textbook, i.e. belong in the same "box" as the physics textbook.

In some sense, you are performing a **mapping** in your head. The subject textbook is the information you have, and you need to determine which notebook you need to take out, based on that. Let the mapping that lets you determine the notebook based on the textbook subject be $$f,$$ and the mapping that lets you determine the textbook based on the notebook subject be $$g.$$

Consider the box (in the diagram), labelled Grammar. Grammar has the following objects under its label: a grammar notebook, and a grammar textbook. 

In what way(s) can I perform mapping $$f$$ now? If I had my grammar textbook (T), I would know I need my grammar notebook (N) as well, with $$f.$$ You can write this as $$T \rightarrow N.$$

In what way(s) can I perform mapping $$g$$ now? If I had my grammar notebook (N), I would know I need my grammar textbook (T) as well, with $$g.$$ You can write this as $$N \rightarrow T.$$

However, I don't need to be devious enough to make you "guess" which notebook/textbook is required based on the information you have. You could just be directly told: "Bring your Grammar Notebook", or "Bring your Grammar Textbook". That way, you are acting on the information you are given, and give back the same information. You able to exactly identify what you need to do. We call these "direct" instructions identity mappings. Here, we can define two identity mappings, $$i_{t}$$ and $$i_{n}$$ which are the identities of the "grammar textbook" and "grammar notebook" objects respectively.

I could also be really cruel and be painfully confusing. I could ask you to "Bring the textbook that corresponds to the notebook of your grammar textbook".

How would you go about figuring out which textbook to bring? First, you would try to find out what is the notebook that corresponds to your grammar textbook. Applying the definition of $$f,$$ this would be your grammar notebook. This simplifies the statement to "Bring the textbook that corresponds to your grammar notebook". Applying the definition of $$g,$$ you now know you need to bring your grammar textbook.

This convoluted example is a demonstration of "composition". If you noticed, you are performing one mapping inside another mapping. Here, we have actually performed $$g(f(x)),$$ or $$g \circ f.$$ When using the bracket or $$()$$ notation, the mapping you need to perform first in order to make sense of the sentence appears inside, and the mappings you need to perform on that value appear outside.

In this example, we now have four mappings: $$i_{t}, i_{n}, f$$ and $$g.$$

**Exercise 1:** Using our definition of mappings, and composition, try to find out what $$i_{t} \circ (f \circ g)$$ and $$(i_{t} \circ f) \circ g$$ is. Do you notice anything? Do you identify a problem? Remember that operations in brackets will need to be performed first!

**Spoiler:**
<details> You will run into a problem! Why? </details>

**Exercise 2:** Using our definition of mappings, and composition, try to find out what $$f \circ (g \circ f)$$ and $$(f \circ g) \circ f$$ is. Do you notice anything? Do you identify a problem? Remember that operations in brackets will need to be performed first!

**Spoiler:**
<details> You shouldn't run into a problem. In fact, you will realize $$f \circ (g \circ f) = (f \circ g) \circ f.$$ </details>

## 🔁 Mathematical Definition of a Category

Surprise, surprise, Subjects is NOT a Category! This is because it does not satisfy something known as "associativity of composition". In **Exercise 1,** notice that changing the brackets affects the final answer. That must not happen in a category.

Like discussed in [about this blog](https://popularcategorytheory.github.io/aboutblog/), the dictionary definition of a “category” is: “a class or division of people or things regarded as having particular shared characteristics”, which means a everything in a category is related to each other in some way or the other. This act of "relating" is captured through mappings. 

So, what actually is a category?

**Definition.** A Category $$C$$ has the following data:

1. Objects: $$A, B, C, D$$ etc.
2. Mappings: $$f, g, h$$ etc.

Each of these objects has a mapping that maps the object back to itself. You can think of these as the identity mappings we defined earlier for "Grammar Textbook" and "Grammar Notebook". In mathematical terms, identity mappings must exist for each of these objects. Another criteria that identity mappings need to satisfy is that $$i_{a}\circ f = f = f \circ i_{a}$$ for any identity mapping $$i_{a}.$$

Say you have two mappings, $$f$$ and $$g$$ such that $$f$$ inputs $$A$$ and outputs $$B,$$ and $$g$$ inputs $$B$$ and outputs $$C,$$ then you should be able to define $$f \circ g,$$ or the composition of $$f$$ and $$g.$$ You should be able to compose mappings whose output matches the other's input.

Like discussed earlier, composition of mappings must be associative. This means $$(f \circ g) \circ h = f \circ (g \circ h).$$

# 🤔 For the Philosophers

Now, imagine that subjects were indeed a category. Imagine that I had several boxes, all satisfying the definition of a category, and the category was labeled mathematics!

The definition of a category itself is quite interesting in a sense. The technical definition is entirely built on the simple, english definition of the word. The structures actually represent thinking in itself, as outline in [about this blog.] (https://popularcategorytheory.github.io/aboutblog/)(And yes, I'm stressing that link repeatedly since it must be read before this post.)

An application of Category Theory into societal issues is outlined in Eugenia Cheng's talk on [Category Theory in Life](https://www.youtube.com/watch?v=ho7oagHeqNc)

# 🖥️ For Those Interested in Computer Science

TYPES! The most obvious example of a categorical framework in Computer Science is in programming languages. Another connection between programming languages and Category Theory, that I personally find to be a very intriguing field of research, is [Lambda Calculus](https://en.wikipedia.org/wiki/Lambda_calculus)

# ✨ Conclusion

Congratulations! 🥳

You now know what a category is, what the data in a category is, and exactly what rules a category needs to satisfy. You have also been briefly introduced to (comparitively trivial) applications of Category Theory outside of mathematics!

We're not tired of the abstraction just yet! We don't just say that Category Theory gives a birds' eye view of mathematics (and arguably, everything) for nothing!

Next Stop: Functors.








