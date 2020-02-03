---
title: "My run in with groupings"
tags: [Visual Studio, C#]
---

[tab]At work, I saw a collection set up that was unfamiliar to me. This collection was the IGrouping expression. At first, glance that the groupby extension was using a lambda expression to create a list of objects. The objects are sorted by the expression orederby used on the collection.
[tab]That was not the full story, using my copy of "C# 6.0 in a Nutshell The Definitive Reference" their explanation is "Enumerable.GroupBy works by reading the input elements into a temporary dictionary of lists so that all elements with the same key end up in the same sublist. It then emits a sequence of grouping. A grouping is a sequence with a key property." I looked at it as a dictionary where each key pointed to a list collection. Originally I had planned to rewrite. It seemed messy and bloated. At first, the explicit type of IEnumerable<IGrouping<TKey, TElement>> and the looping strategy for this collection seemed like a lot. It was the best thing to use for the structure we were passing to a pie chart view.
[tab]After working with it, this is a structure I plan to use again.  Below a code snippet and an example of its usage.
