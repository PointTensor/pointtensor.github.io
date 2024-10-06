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

**Mathematical efforts**

Indeed, the idea of treating History as part of the hard sciences is not new. Professor Peter Turchin, a biologist turned complexity scientist, is one of the founders of the field of cliodynamics. This interdisciplinary field aims to build mathematical models of history and its processes by combining various components which are thought to contribute to such processes such as, economic history; cultural evolution; macrosociology; etc. Turchin and his collaborators aim to answer questions like why some empires grow and prosper, while others fall from grace and die off. Turchin and others in Cliodynamics may use information about tax, measurements of bones to find the average height of a historical population, or archeological evidence that could be converted into facts usable in a mathematical model.  

Mathematical models have proved extremely effective in the natural sciences where a purely verbal approach is inadequate. Mathematical models allow us to clearly identify the components needed for such studies, they provide us with the means to build quantifiable models and test our hypotheses empirically against real-world data. Historians now have access to a huge corpus of knowledge, allowing them to use machine learning techniques to uncover hidden patterns in data and possibly better elucidate the historical events that they study.

Dynamical systems, like the ones Turchin studies, can exhibit chaotic behaviour. Normally, dynamical systems like those describing the trajectory of a ball do not exhibit `unexpected' results. When one changes a parameter in our equation, say the mass of the ball, the trajectory does not drastically change. If the trajectory resembles a parabola, then the new trajectory of the ball with a slightly different mass will still be a parabola, albeit slightly shrunk or stretched. One can reliably predict the path of the ball for all times. Chaotic systems on the other hand exhibit extremely sensitive dependence on the parameters in the equations. A small change in one of the parameters can lead to completely different behaviour. It would be like the ball suddenly starts going along an arbitrary trajectory as one changes the mass.  The trajectory no longer retains its parabolic shape as time goes by. We can also think of applying the same example on multiple balls with dependencies on each other’s movements and parameters. History seems to be chaotic, unpredictable; small and insignificant events lead to unforeseen large-scale consequences. The incident of assassinating one leader from the Austro-Hungarian empire, for example, resulted in WWI in which millions have died. The question is then, how can we capture such traits mathematically?

**Chaos, self similarity, and unpredictability**

I will single out three apparent issues pertaining to predicting historical events. These are:

* Chaotic behaviour
* Unpredictability
* Self-similarity

We are assuming here that a set of related historical events have been analysed and modelled mathematically. We then found that the system behaviour has many features or issues including these three, that represent our notion of history repeating itself. 

**Complexity from a simple equation**

All three traits above are interlinked. I would like you, the reader, to understand that unpredictability does not imply randomness. Let us illustrate that with a toy-model from a paper by George A. Reisch (Chaos, History, and Narrative). Suppose a biology student goes on a field trip to record the population of a certain species. He or she records the population at the end of every season and plots them as shown in figure \ref{fig:observed}.

<!-- \begin{figure}[h]
    \centering
    \includegraphics*[scale=0.6]{images/history_modelling/student_record.png}
    \caption{Observed population levels.}
    \label{fig:observed}

\end{figure} -->

![Observed population levels\label{fig:observed}](ralawadhi.github.io/assets/images/historical_modelling/student_record.png)