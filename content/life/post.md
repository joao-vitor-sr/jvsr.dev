+++
title = "Katex rendering"
description = "How to render katex"
date = 2019-10-30

[extra]
katex = true
+++


This post is the synthesis of, on one hand, the programmer undergraduate at
mathematics who spent most of his life trying to resist being fooled by
randomness and trick the emotions associated with uncertainty.

I'm not capable of avoiding being the fool of randomness; what I can do is
confine it to where it brings some aesthetic gratification.

## The Medical Test Paradox

I want to explore a very special paradox in medical tests (have in mind that I'm
a programmer and an undergraduate mathematician, so don't take this so seriously, I
want to explore the math, not the mind behind doctors), think about a test,
which is highly accurate, which means that this test provides correct results
for most people, have in mind that accuracy does not mean that it's predictive.

The usual thinking about math is not as a thinking process, instead, common sense
says that math is a "fix" thing, that it's not organic, even the vision of a
mathematician by the crowd is an anemic man with a shaggy beard and grimy and
uncut fingernails silently laboring on a Spartan but disorganized desk. With
thin shoulders and a pot belly, he sits in a grubby office, totally absorbed in
his work, oblivious to the grunginess of his surroundings. He grew up in a
communist regime an anemic man with a shaggy beard and grimy and uncut
fingernails silently laboring on a Spartan but disorganized desk. With thin
shoulders and a pot belly, he sits in a grubby office and speaks English with an
astringent and throaty Eastern European accent. When he eats, crumbs of food
accumulate in his beard. With time he becomes more and more absorbed in his work,
oblivious to the grunginess of his surroundings.
I want to dig in on this paradox.

### What's the paradox

Picture 1.000 People, and let's say that 1% of them have a rare disease, all
those 1.000 people go under some kind of test, and 9 (of the 1%) have a true
positive and 1 (again from the 1% or 10) is a false negative, and 89 of
the remainder receives a false positive, and the rest (901) have true
negatives.

Think that you know some of those people, and they go under the test and get a
positive result, you don't know anything about sympthons or anything similar,
there are only two options here, or this person is one of the 89 with false
positives or is under the 9 true positives.

££
P \sim \frac{9}{9 + 89}
££

In medicine (from what I know), this is called P.V.V, and this gives us the insight
that probability is much harder than what you usually think, in this case,
just by the result, we don't know in which group the person is at the
false positive ones, or the true positive.

#### A Example

This is complicated since in all possible places for math being counterintuitive,
this is one of them that matters, and matters a lot. The psychologist Gerd Gigerenzer
made a series of seminars involving statitics, one of which is the following example.

__"A 50-year-old woman, with no symptoms, participates in routine mammography screening.
 She tests positive, is alarmed, and wants to know from you whether she has
 breast cancer for certain or what the chances are.

 apart from the screening results, you know nothing else about this woman"__

If you found this example similar to the one that I presented to you, it's from this
seminar that I got the idea.

1. The prevalnce of the test is 1%.
2. The Sensitivity is 90%
3. The Specificity: 91%

You probably already know the answer, which is
££
\frac{1}{11}
££
but the doctors didn't know about the math behind, that there're 1.000 people that
applied to the same test, etc.

all they saw was those numbers, they were asked, which are the chances that
this woman has breast cancer, and they were presented with four choices for
answers

1. 9 in 10
2. 8 in 10
3. 1 in 10
4. 1 in 100

In one of the sections, over half of the doctors chose the answer number one,
which is far from reality.

This in mathematics is a Veridical Paradox

1. Probably true
2. Seems false

The question is, how we can combat this

## Our genes

I will not delve too deeply, into the amateur evolutionary theory to probe at the
reasons (besides, despite having spent some time in libraries I feel
that I am truly an amateur in the subject matter). The environment
for which we have built our genetic environment isn't the one that prevails
today. By genetic standards, these Homeric heroes of 30 centuries ago in all
likelihood have the identical genetic makeup as the pudgy middle-aged man
you see schlepping groceries in the parking lot. More than that. we are
truly identical
 perhaps 80 centuries ago started being called "civilized", in that strip of land
 stretching from Southeastern Syria to Southwestern Mesopotamia.

## You Should be Dead by now

This brings to mind another common violation committed by "gurus, coaches, masters"
on the internet, who may be selected for their looks, charisma, and their
presentation skills, but certainly not for their incisive minds. It's the
following fallacy: "An average person is expected to live 73 years, therefore
if you're 68 you can expect to live five more years, and should plan
accordingly". Now, what if you're 80? Is your life expectancy minus seven years?
What these journalists confuse is the unconditional and conditional life expectancy.
At birth, your unconditional life expectancy maybe 73 years. But as you advance
in age and do not die, your life expectancy increases along with your life. Why?
Because the other people dying have taken your spot in the statistics. So if
you are 73 and are in good health, you may still have, say, nine years in
expectation. But the expectation would change, and at 82, you will have another
five years, provided of course you are still alive.

## Bayes theorem

Now we reach the Bayes theorem, one of the most important in randomness,
this theorem is central to scientific research, it's the core of AI, and much more.

thin of a man called Steve. The unique thing that I'll say about Steve,
is that he is very shy, now which career Steve will work on? A Math Ph.D. Or
Business School. I'm sure that most would choose Ph.D. in Math, even those who chose
Businesses don't know to answer why, may not be so obvious, but everybody
thinks that a shy person would do better in math instead in business.

This is the problem with your beliefs, in this case, stereotypes, don't think about the
person, but first, think about the probabilities involved. Now with the knowledge that you may have,
and not trying to find an official definition, what's the total relation between math Ph.D. students,
and business students, it's obvious that we have more business students than
math ones, let's say in a relation of 10 to 1, look around how many
math students have you met? Unless you're involved in math, probably you have
met more business students.

Think that we have 1.000 students, and 100 of them are in the math field,
and the rest is on business, 75% of the students in math are shy, but
15% of the business are shy, in other words, we have *75 students of math* tht
are shy, and *135 students of business* are shy.

the chances of Steve being in the business field still is double than the
math.

And, this is the error that you commit every day, every time you read something,
or read the news, and see probabilists, and statistics, you ignore the hidden information,
you think that you're rational, but you are not actually, and this is the most
important thing about Bayes, even if you never use the formulas.

## We're fools at math

It's always possible to combine random data, and find some regularity in them,
one example is the coincidence between Lincon and Kennedy,

two presidents, with seven letters on the last names, were elected with
100 year of difference, both died on Friday, in the presence of their wives,
Lincoln on a ford theater, and Kennedy on a car produced by ford.

Bizarre no? but if we compare other important attributes we fail at finding
coincidences. People live decades, with millions of events along their life,
you **always** will find coincidences between any two persons.

How many times have you met a person at a party and thought: "wow, how we have so much
in common", and you think the fallacy of "oh, it's the destiny, we were made to meet", Nah,
it's not, talk with anyone else at the same party, and you will find the same situation.

## Conclustion

The reader may know my opinion on unsolicited advice and sermons on how to behave
in life. Recalt ideas do not truly sink in when emotions come into play; we do not
use our rational brains outside of classrooms, and Self-help books (even when they
are not written by charlatans) are largely ineffectual. Good, enlightened (and
"friendly") advice and eloquent sermons do not register for more than a few
moments when they go against our wiring. The interesting thing about stoicism
is that it plays on dignity and personal aesthetics, which are part of our genes.
start stressing personal elegance at your next misfortune. Exhibit sapere vivere
in all circumstances.

Dress at your best on your execution day (shave carefully); try to leave a good
impression on the death squad by standing erect and proud. Try not to play the victim
when diagnosed with cancer (hide it from others and only share the information
with the doctor - it will avert the platitudes and nobody will treat you like
a victim worthy of their pity; in addition the dignified attitude will make both
defeat and victory feel equally heroic). Be extremely courteous to your assistant
when you lose money. Try not to blame others for your fate, even if they
deserve blame. Never exhibit any self-pity, even if your significant other
bolts with the handsome ski instructor or the younger aspiring model.
Do not complain. If you suffer from a benign version of the "attitude
problem". Good luck.

