---
title: Can't Stop Calculator
description: 
date: 2024-07-21
tags:
  - Can't Stop
  - Interactive
---

*This is the first of my interactive posts. If you have any requests for interactive posts like this, please leave them below in the comment box!*

*This post assumes you have an understanding of how to play **Can’t Stop.** You can read a copy of the rules on [BoardGameGeek](https://boardgamegeek.com/boardgame/41/cant-stop).*

After playing a few dozen games of **Can’t Stop** on BoardGameArena, I decided to build a calculator to see if my intuitive feeling of the percentages matched up with reality. 

## Calculating Bust Probability

The first step is to identify what we are looking for. When playing **Can’t Stop**, the most useful information is the *bust probability*. Bust probability is a function of two variables: *completed tracks,* and *in-progress tracks*. *Completed tracks* is a list of all tracks that have reached the top. *In-progress tracks* is a list of all tracks that the current player is currently climbing. From these, a list of *valid sums* can be calculated: if there are fewer than three in-progress tracks, this is a list of all non-completed sums. If there are three in-progress tracks, then it is the in-progress sums minus any “tentatively complete” sums. 

Next, I need to calculate all *possible combinations* of the dice. In total, there are 1,296 different rolls for four dice — 6^4. For each of these, there is between one and six possible sums to choose from. Lastly, I need to divide the possible combinations with a valid sum by *all* possible combinations. This is your chance of busting!

## The Calculator

<p class="codepen" data-height="550" data-default-tab="result" data-slug-hash="gOEqKRw" data-pen-title="Can't Stop Calculator" data-user="AdamGiese" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/AdamGiese/pen/gOEqKRw">
  Can't Stop Calculator</a> by Adam Giese (<a href="https://codepen.io/AdamGiese">@AdamGiese</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>