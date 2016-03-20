---
layout: mathpost
title: CALENDARS & FRACTIONAL APPROXIMATION
date: 2016-01-16
categories:
- math
- math.NA
---

{% raw %}
Have you ever wondered what a calendar <i>is</i>? How would you explain the notion of a calendar to an alien, albeit a very precocious one with some notion of homo sapiens common sense?

The word <i>calendar</i> originates from Latin <i>calendae</i> , or "calends". The calends was the first day of the month in the ancient Roman calendar, when the debts fell due and accounts were reckoned in accordance with the account book called <em>kalendaria</em>.

A calendar is a systematic register of time. At the core of the solar calendar lies a notion of a day, or the period of the Earth complete rotation about its axis, and a year, or the period of the Earth moving in its orbit around the sun.

In the common calendar, each day is assigned a unique date which corresponds to a particular day, month and year. One-to-one correspondence is established between a date and a certain period of time, serving a function of a complete and consistent register of human experience. There are several calendric systems fulfilling one purpose or another:

<ul>
    <li>fiscal calendars are used for budgeting, keeping accounts and taxation</li>
    <li>religious calendars (e.g. Hebrew, Islamic) are used to determine dates of religious significance</li>
    <li>civil calendars (e.g. Gregorian, Julian) are used for general purposes, such as synchronisation of logistics and business administration.</li>
</ul>

The calendar commonly adopted for general purposes is the Gregorian calendar.

<h1>Gregorian Calendar</h1>

<strong>Fractional Approximation</strong>

<p style="text-align:left;">
To understand the underlying structure of any calendric system we need some vocabulary. All solar calendars are based on the time period in which the Earth completes a full seasonal circuit called the <i>tropical year</i>. As of the year 2000, the mean tropical year is 365.242189 [1]. Although the duration of the tropical year changes, assume that it is known precisely. Note the fractional part 0.242189. 

Let's say we want our year to last 365 days. Every time we the year finishes, the error term is introduced. If the error was not adjusted in the long term, some time later the ignorant astronomer from New York or Kostroma would be freezing in July snow and drip sweat in the flourishing park in January! But how can the fractional part be approximated in such a way that the discrepancy with the accurate value is minimal? The problem of the calendar construction in other words can be simplified as follows:</p>

<p style="text-align:center;"><em> Find an approximation of a real number</em>
<em> in the form of a fraction with the denominator q.</em></p>

<p style="text-align:left;">If the real number line is constructed and all the rational numbers with the denominator q are marked on it, the number $ \alpha $ is either equal to one of the fractions or lies between two of them. The case of  $ \alpha $ coinciding with one of the fractions is trivial.However, if $ \alpha $ is not equal to either of them, it satisfies the following pair of inequalities for some integer p:</p>

<p style="text-align:center;">$\frac{p-1}{q} &lt; \alpha &lt;\frac{p}{q}$</p>

One of the two fractions $ \frac{p-1}{q}$ and $ \frac{p}{q} $, which is closer on the number line to $ \alpha $, constitutes the best rational approximation with the required denominator $ q $. For instance, let's consider the approximation of  represented in Figure 1.
{% endraw %}
<p>
<ul style="list-style-type:none; display:table;margin:auto;text-align:center;">
<li><img src="{{ site.baseurl }}/assets/drawing.png" width="256px"/></li>
<li> <em>Figure 1</em></li>
</ul>
</p>
{% raw %}

$ \alpha $ is closer to $ \frac{p}{q} $, and hence $ \alpha\approx\frac{p}{q} $.  If $ \alpha $ lies exactly between $ \frac{p-1}{q} $ and $ \frac{p}{q} $, $ \alpha $ is said to be best approximated by $ \frac{p}{q} $ to eliminate indeterminate cases. When $ \alpha $ is approximated, a corresponding approximation error $ \Delta $ emerges:

<p style="text-align:center;">$ \Delta=\alpha-\frac{p}{q} $</p>

If the approximation $ \frac{p}{q} $ underestimates $ \alpha $, $ \Delta &lt; 0$ , if  it overestimates, $ \Delta &gt; 0$ .
The absolute value of the approximation error, $ |\Delta|$, is called an <em>absolute error</em>.

From Figure 1 it is evident that the absolute error never exceeds half the length between the approximating fractions. Thus,

<p style="text-align:center;">$ |\Delta| \leq \frac{1}{2q}$</p>

The value $ \frac{1}{2q}$ is the <em>upper bound</em> of the absolute error. The upper bound of the absolute error is achieved when $ \alpha$ lies exactly between the approximating fractions.

<p style="text-align:left;">The approximation is optimal, if for the relatively small denominator $ q$ the approximation is as close to the true value as possible. This condition can be characterised by comparing the absolute error and its upper bound:</p>

<p style="text-align:center;">$ | \alpha - \frac{p}{q}| : \frac{1}{2q}=2|q \alpha-p| $</p>

The defining part of the above equation is $ |q\alpha-p|$. Let's call this value the <em>reduced error</em> $ h$. Since the ratio of the absolute error to the upper bound of the absolute error lies between zero (in which case the approximation approaches the true value) and one,

<p style="text-align:center;">$ 0&lt;h \leq \frac{1}{2} $</p>

The smaller $ h$, the more preferable the approximation is. Let $ \lambda$ be the <em>coefficient of optimality</em> defined as

<p style="text-align:center;">$ \lambda=\frac{1}{2h}=\frac{1}{2|q\alpha-p|}$</p>

The coefficient of optimality can be intuitively understood as the factor by which the absolute error is less than the upper bound of the absolute error. Thus, the greater $ \lambda$, the more preferable the approximation is. From (6) it follows that $ 1\leq\lambda&lt;\infty$ and $ \lambda h=\frac{1}{2} $.

How can we apply the idea of fractional approximation to the development of a solar calendric system? We will find out soon. Let's acquiant ourselves with a wonderful tool in our mathematical apparatus.

Let's forget about the decimal number system. A mathematician Nikolai Nikolaevich Luzin said: "The advantages of the decimal number system are not mathematical but zoological. If humans had eight fingers instead of ten, the humankind would use the octal number system." The decimal number system is useful in everyday life, but its use becomes superfluous if theoretical questions of arithmetic are investigated.
Thus, we give up on using any specific base and focus on the following question: what is the most intuitive way of approximating a non-integer number?
The answer seems to be straightforward: determine an integral interval (interval between two integers) which contains the approximated number. The number hence can be represented by identifying the lower bound of the interval:

$$ \exists(\alpha\_0 \in N,\  0 &lt;r&lt;1)(\\alpha \approx \\alpha\_0+r)$$

$ \alpha\_0 $ is our first approximation. Since $ r$ is less than 1, it can be represented in the form $ r=\frac{1}{x\_1}$, where $ x\_1$ is greater than 1. Hence, (9) can be written in the following form:

$$ \exists (\alpha\_0,\in\mathbb{N}, x\_1&gt;1)(\alpha \approx \alpha\_0+\frac{1}{x\_1})$$

Now our approximation can be improved even further; we can repeat the procedure for approximating $ x\_1$. Thus we obtain:

$$ \exists (\alpha\_0,\alpha\_1\in\mathbb{N}, x\_2&gt;1)(\alpha \approx \alpha\_0+\frac{1}{\alpha\_1+\frac{1}{x\_2}}). $$

The expression 
$$ \alpha\_0+\frac{1}{\alpha\_1+\frac{1}{\alpha\_2+\frac{1}{\cdots+\frac{1}{\alpha\_{n-2}+\frac{1}{{\alpha\_{n-1} +\frac{1}{\alpha\_n}}}}}}}$$ 
is called a continued fraction. $ \alpha\_0, \alpha\_1, \cdots, \alpha\_n$ are called the <em>elements</em> of the continued fraction. We restrict the current definition to $ \alpha\_0, \alpha\_1, \cdots, \alpha\_n \in \mathbb{N}$. Note the gawky notation which can be tedious to write on a piece of paper if there are more than, for instance, 5 elements. Let's introduce the short-hand notation so that  our continued fraction can be written in the following form: $ [\alpha\_0;\alpha\_1,\alpha\_2,\cdots,\alpha\_n]$.

The following theorems can be proven:

<ul>
    <li>Any positive rational number can be represented as a unique continued fraction with a finite number of elements and the last element equal to one.</li>
    <li>Two continued fractions are equal if and only if their corresponding elements are equal.</li>
</ul>

Irrational numbers cannot be represented as a finite continued fraction. However, there is a representation of each irrational number as a string of natural numbers in the form given above.

Each continued fraction can be broken down into a <em>fit fraction</em> by writing down its first <em>n</em> elements and discarding all the others. The smaller <em>n</em>, the <em>simpler</em> the fit fraction is, i.e. it has a smaller denominator. The magnificent property of fit fractions is that <em>any</em> other approximation of <em>any</em> number by <em>any </em>fraction with the smaller denominator is worse than the approximation by a corresponding fit fraction.

The proofs are omitted in the present discussion; rigorous development and further comprehensive  study of continued fractions can be found in the book by A.Ya. Khinchin.

<strong>Application to the Tropical Year</strong>

Let's return to our original problem. We need to approximate as closely as possible the mean length of the tropical year, $ y=365.242189$.

Wouldn't it be convenient for the length of the year to be such a nice integer 365? Nothing stops us to make our own conventions! Yet here is the downsize: our value would lose its physical meaning. Each 'year' the Earth would be found in a different point of its orbit! In four years the discrepancy would constitute almost a whole day. This inconvenience destroys all our hope for the practical method of time accounting, doesn't it?

It does not. Let's devise the solution, remembering about the <a href="https://en.wikipedia.org/wiki/KISS\_principle">KISS principle</a>.

$ y$ can be represented as the following continued fraction (verify!):

$ [365; 4, 7, 1, 3, 40, 2, 3, 5]$

Let's calculate all the fit fractions.

$ \frac{p\_0}{q\_0}=365$
$ \frac{p\_1}{q\_1}=365+\frac{1}{4}=365\frac{1}{4}$
$ \frac{p\_2}{q\_2}=365+\frac{1}{4+\frac{1}{7}}=365\frac{7}{29}$
$ \frac{p\_3}{q\_3}=365+\frac{1}{4+\frac{1}{7+\frac{1}{1}}}=365\frac{8}{33}$
$ \frac{p\_4}{q\_4}=365+\frac{1}{4+\frac{1}{7+\frac{1}{1+\frac{1}{3}}}}=365\frac{31}{128}$
$ \frac{p\_5}{q\_5}=365+\frac{1}{4+\frac{1}{7+\frac{1}{1+\frac{1}{3+\frac{1}{40}}}}}=365\frac{1248}{5153}$

$ \frac{p\_6}{q\_6}=365+\frac{1}{4+\frac{1}{7+\frac{1}{1+\frac{1}{3+\frac{1}{40+\frac{1}{2}}}}}}=365\frac{2527}{10434}$

$ \frac{p\_6}{q\_6}=365+\frac{1}{4+\frac{1}{7+\frac{1}{1+\frac{1}{3+\frac{1}{40+\frac{1}{2+\frac{1}{3}}}}}}}=365\frac{8829}{36455}$

$ \frac{p\_6}{q\_6}=365+\frac{1}{4+\frac{1}{7+\frac{1}{1+\frac{1}{3+\frac{1}{40+\frac{1}{2+\frac{1}{3+\frac{1}{5}}}}}}}}=365\frac{46672}{192709}$

We obtain the following table:

<table border="1" style="width:100%;">
<tr>
    <th>Number</th>
        <th>Leap Years</th>
    <th>Mean Year Length</th>
    <th>Error</th>      
</tr>
<tr>
    <td>1</td>
        <td>1 leap year for every 4</td>
    <td>365 days 6 hours 0 minutes 0 seconds</td>
    <td>-11 min 15 s</td>       
</tr>
<tr>
    <td>2</td>
    <td>7 per 29</td>
    <td>365 d 5 h 47 min 35 s</td>      
    <td>+ 1 min 10 s</td>
</tr>
<tr>
    <td>3</td>
    <td>8 per 33</td>
    <td>365 d 5 h 49 min 05 s</td>      
    <td>- 20 s</td>
</tr>
<tr>
    <td>4</td>
    <td>31 per 128</td>
    <td>365 d 5 h 48 min 45 s</td>      
    <td>+ 0.13 s</td>
</tr>
<tr>
    <td>5</td>
    <td>1248 per 5153</td>
    <td>365 d 5 h 48 min 45 s</td>      
    <td>+ 0.13 s</td>
</tr>
</table>

Changes in the optimality of all the other approximations are insignificant up to a second. Each new fit fraction gives a better approximation of the tropical year. In fact, the approximation number 1 is a backbone of the Julian calendar. With the help of Sosigenes of Alexandria, Julius Caesar ordered the adoption of a calendar with an added day once in four years in the Roman Empire. Omar Khayyam, a prolific mathematician, astronomer, philosopher and poet, suggested the adoption of the more accurate calendar with 8 leap years per 33-year cycle.

Discrepancy of 130 milliseconds in the 4th approximation has no practical importance in casual use. It is much more accurate than the Gregorian year, which is precisely 365 days 5 hours 49 minutes and 12 seconds, lagging behind the tropical year by about 27 seconds. Yet the adoption of such a calendar is problematic: the occurence of leap years is not <i>round</i>, and transcendence of the cultural and administrative barriers requires a great leap from the humankind.

<strong>BIBLIOGRAPHY</strong>

<ol>
    <li>Meeus, J. and Savoie, D, <em>T</em>h<em>e history of the tropical year</em>. Journal of the British Astronomical Association, 102(1), 40-42.</li>
    <li>Khinchin, A.Ya. <em>Continued Fractions. </em>The University Chicago Press, 1964</li>
        <li>Beskin, N.M. <em> Continued Fractions. </em> KVANT magazine #1, 1970</li>
</ol>
{% endraw %}
