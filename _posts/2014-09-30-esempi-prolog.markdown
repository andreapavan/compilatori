---
layout: post
title:  "Primi esempi con Prolog"
date:   2014-09-30 15:25:15
categories: Prolog
---

Concatenatore(append) di liste:

{% highlight prolog %}
app([],Xs,Xs).
app([X|Xs],Ys,[X|Zs]):-
	app(Xs,Ys,Zs).
{% endhighlight %}

Rimozione di elementi in posizione pari da una lista:

{% highlight prolog %}
osl([],[]).
osl([X],[X]).
osl([X,_|Xs],[X|Zs]):-
	osl(Xs,Zs).
{% endhighlight %}

Last:

{% highlight prolog %}
last_element([X],X).
last_element([_|Xs],Y):-
	last_element(Xs,Y).
{% endhighlight %}