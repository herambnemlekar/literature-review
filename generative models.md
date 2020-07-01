## Modeling players

1. [Generative Agents for Player Decision Modeling in Games](http://julian.togelius.com/Holmgard2014Generative.pdf)
	- This paper describes an approach to modeling, grouping and interpreting players based on their inferred utility function modeled through reinforcement learning in the form of a generative agent.
	- Uses trained Q-learning agents with manually configured reward parameters as a priori defined personas.
	- Player modelling: description, prediction, interpretation, and in some cases reproduction of player behavior 
	- Dungeons were generated via constrained genetic algorithms
	- Assumptions: The first assumption is that players exhibit a particular de-cision making tendency or style when playing a particularlevel or game, and that this tendency can be captured andexpressed  by  approximating  autility  functionthat  shapestheir  decisions  in-game
	- Comments: Showing summary scrren of previous level, limited the notion of "best" to some combination of the features shown in the summary.
	- For each player's play-trace, we replay the whole game and at each point in time,we input the state description to all of our artificial agents,and compare the player’s decision to the decision of the dif-ferent  agents. the  met-ric  was  calculated  as  the  number  of  agent-persona/humanplayer agreementsNafor each decision made in the humandecision trace, normalized with respect to the number of de-cisions  in  the  player’s  decision  traceN,  i.e.Na/N
	- Future work: Personas may change over time. A person who is collecting all treasures at the start, may start taking shortest path to exit if they get bored.