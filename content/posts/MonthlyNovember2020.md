---
title: "This month in AvaFrame - November 2020 edition"
date: 2020-11-29T20:19:18+01:00
draft: false
slug: "monthlynov2020" 
---

Welcome to our next monthly update. 

+ This month started with the exciting (at least for us :-) ) release of
  version 0.1. Head over to our [github repository](https://github.com/avaframe/avaframe) 
  and our [documentation](https://docs.avaframe.org/en/v0.1) to learn more about
  it (or read our last [post](https://avaframe.org/posts/version0_1/)).

+ With this release (and the rest of the month as well) we improved our
  documentation quite a lot. New *getting started* and *installation* pages
  should make it possible for you to get started (*ha, who would have
  guessed*..) with AvaFrame. To make it more readable we reordered the modules
  documentation. Just recently we started adding the API documentation with all
  our functions as well (for those interested: this is achieved with sphinx
  autodoc/autosummary and docstrings). To acknowledge the (very important) data
  providers, a data sources page was added, with sources and references to data
  we use in our framework.

+ Our existing test cases received more features, now we include multiple
  release areas and multiple scenarios per avalanche. Also included are scenarios
  with resistance areas for our main dense flow avalanche kernel.

+ The first data for real avalanche test cases has made it to the
  repository. So far we concentrated on idealised cases, but we now include 6
  real world avalanches. For now release areas and DEMs are available. Soon these
  cases will also end up in our test scripts.

+ New functions for probability / parameter range simulations are available for
  the dense flow kernel com1DFA. Testing this with an applied example is underway at
  the moment. 

+ We started working on the implementation of our dense flow kernel com1DFA in
  python. This means digging deep into the programming and theory of our C++ reference
  code. The base structure is already there, current developments concentrate on the
  implementation of 2D SPH for depth integrated equations on a surface living in
  3D and time discretizations, among others. Head over to our 
  [github issues](https://github.com/avaframe/AvaFrame/issues/) to get an idea about
  the issues (..ha..) at hand.

+ And finally: the second steering committee meeting took place. Which reminds
  me, I need to add a page about AvaFrame's organisational structure... So watch
  this space...

On to the next month!
 
Felix
