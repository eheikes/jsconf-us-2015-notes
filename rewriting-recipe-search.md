# "Rewriting recipe search -- a dash of sugar, just a smidgen of graph database" by [Tracy Hinds](https://twitter.com/hackygolucky)

In this talk, Tracy walked through her process of building a recipe collection app and learning from it.

([video](https://www.youtube.com/watch?v=IZONih1l4As))

* Want a good digital recipe collection
  * Google does okay; not as good for discovery
  * Lots of website resources, but not all recipe data is readily available.
  * allrecipes.com comments are very valuable
* Graph theory (nodes and their relationships), specifically Neo4j
  * Inspiration from John Resig's Neo4j [art history database](http://ejohn.org/blog/building-art-history-database-computer-vision/)
  * Nodes & relationships have properties; relationships have direction
* Choices
  * Neo4j has huge community and documentation
  * No good recipe data archive. Looked at APIs like Baked Oven, Edamam, Food To Fork -- all had problems (too much info, not enough, bad units, etc)
* Next
  * Goal: find recipes by inputting ingredients and type of cuisine (dinner, southern)
  * open source the code: [hackygolucky/recipe-modeling](https://github.com/hackygolucky/recipe-modeling) (not yet live)
  * web interface
  * web scraping -- APIs are too costly, don't have enough recipes
* Turn failures into learning & becoming better programmers.
