---
layout: post
author: Rashid Alawadhi
title:  "Modelling History as a Dynamical System, Chaos and Self-Similarity"
date:   2024-10-06 22:20:00 +0400
categories: history, chaos, self-similarity, dynamical-systems
published: true
---

This is an essay I originally wrote to be published on [the Real Sciences magazine](https://real-sciences.com/). Omar Meriwani was a contributor and editor who made some helpful remarks and rephrasing. This essay was born out of my thinking about fractals and their properties such as self-similarity. Modelling history is a difficult multi-discipline endeavour and it would be helpful to coarse grain the problem by finding a sort of consistent patterns that historical records experience. It dawned on me that history *tends* to *repeat* itself, but not *exactly*; like fractals.

_Essay begins here_

‘History repeats itself’, a phrase we so often hear and recognize to be self-evident. After all, history is brimming with examples of historical recurrence. Empires rose and fell, wars erupted, cultural revolutions took off and many more examples. Historical events seem from one point of view to have a cyclical nature. However, these recurring events are not exactly the same. Successive empires rising on top of the ruins of the old ones might have different ideals, different political landscapes, or religions. WWII was not exactly the same as WWI, yet the devastation and aftermath were comparable across both events. Perhaps the phrase with which we started the essay should be read as `History tends to approximately repeat itself'. It might not be as catchy and succinct as the original version, but surely more accurate as a description of history. The purpose of this essay is to explore the topic of historical modelling and attempt to find a useful mathematical description of history's apparent properties such as recurrence, self-similarity, and unpredictability.

Various authors like Ibn Khaldun and his concept of Asabiyya (group solidarity/consciousness), and G. W. Trompf's human nature seemed to explain this recurrence to be the result of properties that individual humans share, namely ‘human nature’. I propose that we abandon the search for a reductionist explanation. For, much like the case of fluid dynamics, even if one knew the rules governing the microstructure, one is not able to make predictions about the macrostructure. That doesn’t necessarily apply to our social systems, as complex systems, or to generalize it to all the features of these systems on macro level, but we can still assume that many of what applies to the micro level cannot explain the macro behaviour of the system. 
Joshua S. Goldstein suggests that political entities such as empires, much like people, experience a midlife crisis-like political instability. Empires rise and prosper until a certain point where overconfidence, tyranny, and internal conflicts between governing bodies set in, resulting in the destruction of the political entity. We are taking this as an example, without verifying if there was a study on complex systems that assumed the similarity between empires and individual humans in terms of aging. As examples of such a phenomenon, he cites the British Empire; the German Empire; and the Soviet Union. Some people might argue that it is the specifics of events in history, `the microstructure' is what history is all about. Perhaps even if that is true in some cases, it does not mean that we are doomed and cannot deduce general laws governing historical evolution. To contrast it with two branches of mathematics, differential geometry is concerned about the local(microstructure) of shapes, while topology is about the global aspects of the shape. Both branches are interlinked and teach us a great deal of things.

# Mathematical efforts

Indeed, the idea of treating History as part of the hard sciences is not new. Professor Peter Turchin, a biologist turned complexity scientist, is one of the founders of the field of cliodynamics. This interdisciplinary field aims to build mathematical models of history and its processes by combining various components which are thought to contribute to such processes such as, economic history; cultural evolution; macrosociology; etc. Turchin and his collaborators aim to answer questions like why some empires grow and prosper, while others fall from grace and die off. Turchin and others in Cliodynamics may use information about tax, measurements of bones to find the average height of a historical population, or archeological evidence that could be converted into facts usable in a mathematical model.  

Mathematical models have proved extremely effective in the natural sciences where a purely verbal approach is inadequate. Mathematical models allow us to clearly identify the components needed for such studies, they provide us with the means to build quantifiable models and test our hypotheses empirically against real-world data. Historians now have access to a huge corpus of knowledge, allowing them to use machine learning techniques to uncover hidden patterns in data and possibly better elucidate the historical events that they study.

Dynamical systems, like the ones Turchin studies, can exhibit chaotic behaviour. Normally, dynamical systems like those describing the trajectory of a ball do not exhibit `unexpected' results. When one changes a parameter in our equation, say the mass of the ball, the trajectory does not drastically change. If the trajectory resembles a parabola, then the new trajectory of the ball with a slightly different mass will still be a parabola, albeit slightly shrunk or stretched. One can reliably predict the path of the ball for all times. Chaotic systems on the other hand exhibit extremely sensitive dependence on the parameters in the equations. A small change in one of the parameters can lead to completely different behaviour. It would be like the ball suddenly starts going along an arbitrary trajectory as one changes the mass.  The trajectory no longer retains its parabolic shape as time goes by. We can also think of applying the same example on multiple balls with dependencies on each other’s movements and parameters. History seems to be chaotic, unpredictable; small and insignificant events lead to unforeseen large-scale consequences. The incident of assassinating one leader from the Austro-Hungarian empire, for example, resulted in WWI in which millions have died. The question is then, how can we capture such traits mathematically?

# Chaos, self similarity, and unpredictability

I will single out three apparent issues pertaining to predicting historical events. These are:

* Chaotic behaviour
* Unpredictability
* Self-similarity

We are assuming here that a set of related historical events have been analysed and modelled mathematically. We then found that the system behaviour has many features or issues including these three, that represent our notion of history repeating itself. 

**Complexity from a simple equation**

All three traits above are interlinked. I would like you, the reader, to understand that unpredictability does not imply randomness. Let us illustrate that with a toy-model from a paper by George A. Reisch (Chaos, History, and Narrative). Suppose a biology student goes on a field trip to record the population of a certain species. He or she records the population at the end of every season and plots them as shown in figure [fig:1](#fig:1).

![#fig:1](/assets/images/historical_modelling/student_record.png#center "Recorded population by the student")*Figure 1: Recorded population by the student*

The population of the species in this example is a variable in our historical model, which is the logistic map equation. 

Notice that after 30 seasons the population experiences a sudden crash that persisted for five seasons. There was no obvious prior warning indicating such a phenomenon. In fact, after recovering around season 35, the population crashes yet again around the 44th season albeit with faster recovery. The student is baffled and tries to look for a reason that caused the crash. There must be some underlying cause. But given the possible number of variables that could cause such a crash it is futile to look for them all. Instead he tries to model the population over seasons using a mathematical equation to help him in prediction the evolution of the population. He writes down

\begin{align}
X_{n+1} = r X_n (1 - X_n),
\end{align}

where $X_n$ is the population in the $nth$ season and $r$ is a positive constant that tells us how fast the population multiplies. For this particular species, we have $r = 4$. The equation is extremely simple, it basically states that the population of the current season depends on that of the previous one. \textit{Past populations affect the behavior of the future ones}. Using the recorded population at season 0, i.e. $X_0$, the student plots the following graph([fig:2](#fig:2)).

![#fig:2](/assets/images/historical_modelling/measured_pop.jpeg#center "Plotted figure")*Figure 2: The blue line traces the points obtained by the logistic map equation*

The equation appears to correctly predict the population crashes despite being extremely simple and taking into account any other variable except for the population itself! Notice how the crashing tends to repeat itself at season 45 and then 55, but the numbers and the time difference between them are not exactly the same. This is much like how history repeats itself but not exactly, as we are working on one feature here which is the population. Indeed, we remind the reader that this is a mere toy example that Professor Reisch cooked up to illustrate how seemingly random changes in nature/history can be captured by simple mathematical equations. To further illustrate the ability of the logistic map to capture traits of history, we turn to its chaotic behavior due to its sensitive independence on the value of $r$. We will go about it in this way: we fix a value for $r$ and then calculate the population at some large value of $n$, say $n=150$. We will call $X_{150}$ the final population $X_{final}$. We will record the final population for different values of the parameter $r$ and see how $X_{final}$ varies accordingly. The graph we plot is called a bifurcation diagram for obvious reasons.

![#fig:3](/assets/images/historical_modelling/chaos.png#center "Bifurcation diagram")*Figure 3: The plot shows the chaotic nature of the population change*


_We are quoting the definition of the bifurcation diagram: “A bifurcation diagram is a plot of this steady state solution versus the control parameter(s) of the map. The sudden appearance of a qualitatively different solution for a system as some parameter is varied is called bifurcation and occurs at bifurcation points”. Volos, Christos, and Viet-Thanh Pham, eds. Mem-elements for neuromorphic circuits with artificial intelligence applications. Academic Press, 2021._

This graph exhibits interesting properties. Note how for values between 0 and 1 of $r$ the population ends up dying. Then between $r=1$ and $r=3$, the final population increases linearly as the value of $r$ increases. Then something interesting happens, at around $r=3$, the final population oscillates between two different values as $r$ varies, i.e. it bifurcates. In fact, as $r$ continues to vary, the two lines emitting from $r=3$ each split again and again until around $r = 3.57$, where chaos sets. Beyond that, the value of the final population exhibits extreme sensitivity to the value of $r$. As $r$ varies, the value of the final population will seemingly randomly jump around. Chaos sets in and it becomes impossible to predict the value of $X_{final}$. Here is the same graph for values of $r$ from 2.8 to 4.

![#fig:4](/assets/images/historical_modelling/bifur28.png#center "Zoomed in bifurcation")*Figure 4: Zoomed in plot showing the chaos boundary*

# Attractors

Another analogy between history and chaotic systems that I would like to address is the concept of attractors. One can think of an attractor as a state towards which solutions(events) tend to evolve. I like to think of historical events such as WWI and WWII to be two different initial conditions that evolved towards an attractor, war. A visual example of a chaotic system with two attractors is the Lorentz Attractor.

![#fig:5](/assets/images/historical_modelling/lorentz_att.jpeg#center "Lorentz attractor")*Figure 5: Plot of a Lorentz attractor*

This is a plot of a solution of specific initial conditions. The starting point, which can be seen to be around the lower middle part of the plot, starts its journey towards the two whirlpool-like areas. The solution, i.e., the line, never actually crosses itself no matter how long we let it journey. It never comes back to exactly where it was in the past, only approximately so; much like history when it `repeats' itself! Let us change the initial conditions and see how the trajectory changes for four different initial conditions

![#fig:6](/assets/images/historical_modelling/lorentzAtt.gif#center "Lorentz attractor for four different initial conditions")*Figure 6: Plot of a Lorentz attractor for four different initial conditions*

The four new solutions are represented by the colours orange, green, and red. Notice how despite starting at different locations on the plot and diverging from each other at different points, they all get attracted toward the two whirlpools. The analogy I would like to draw with historical events is the following. Much like how different events, decisions, environmental factors, etc., that lead to dire consequences yet similar in some sense (WWI and WWII), the Lorentz Attractor and other chaotic systems exhibit something similar.

I think modelling historical events as a dynamical system that enjoys the aforementioned properties can be a step in the right direction of mathematising the study of history. I expect that the majority of traditional historians might object to the idea I am showcasing in this article. After all, they emphasise the importance of individual events, and the stories and narratives they weave with them. Indeed, the goal of this article is not to belittle the accomplishment and hard work of historians, but to bring attention to history's peculiar properties and a way to model them. Individual events are important, yes, but what if they are governed by a more fundamental principle? What if these individual events do not exactly have enough influence to change the course of history? The idea is to study global aspects of history rather than the local. An ant, whether standing on a sheet or a ball, will see a flat surface regardless. Individual events might be forcibly directed and at the mercy of a more global aspect of history.