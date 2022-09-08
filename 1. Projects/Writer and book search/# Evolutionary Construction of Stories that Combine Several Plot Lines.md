---
created: 2022-09-02T16:07:25 (UTC -07:00)
tags: []
source: https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5
author: Gervás, Pablo, Concepción, Eugenio, Méndez, Gonzalo
---

# Evolutionary Construction of Stories that Combine Several Plot Lines | SpringerLink

> ## Excerpt
> Although the narrative structure of common entertainment products like Hollywood movies or TV series is generally composed of a number of different plot lines combined into a single narrative discourse, efforts on computational modeling of story generation have to this point focused mostly on the construction of stories with a single plot line. The present paper explores an evolutionary solution to the task of building a story that combines more than one plot line into a single linear discourse. This requires: a set of knowledge resources that capture the main features that influence the decisions involved, a representation suitable for evolutionary treatment for discourses with several plot lines, and a set of fitness functions based on metrics related to the quality of the resulting discourses. The proposed solution produces populations of stories with elaborate discourses that combine several subplots.

---
## Abstract

Although the narrative structure of common entertainment products like Hollywood movies or TV series is generally composed of a number of different plot lines combined into a single narrative discourse, efforts on computational modeling of story generation have to this point focused mostly on the construction of stories with a single plot line. The present paper explores an evolutionary solution to the task of building a story that combines more than one plot line into a single linear discourse. This requires: a set of knowledge resources that capture the main features that influence the decisions involved, a representation suitable for evolutionary treatment for discourses with several plot lines, and a set of fitness functions based on metrics related to the quality of the resulting discourses. The proposed solution produces populations of stories with elaborate discourses that combine several subplots.

### Keywords

-   Story generation
-   Multiplot stories
-   Evolutionary approach

This paper has been partially funded by the projects CANTOR: Automated Composition of Personal Narratives as an aid for Occupational Therapy based on Reminescence, Grant. No. PID2019-108927RB-I00 (Spanish Ministry of Science and Innovation) and InVITAR-IA: Infraestructuras para la Visibilización, Integración y Transferencia de Aplicaciones y Resultados de Inteligencia Artificial, UCM Grant. No. FEI-EU-17-23.

## 1 Introduction

The narrative structure of common entertainment products like Hollywood movies or TV series is generally composed of a number of different plot lines combined into a single narrative discourse. There are very clear mechanisms at work in putting multiple plot lines together into a successful narrative discourse in this fashion, yet efforts on computational modeling of story generation have to this point focused mostly on the construction of stories with a single plot line. This is in part due to the application of a traditional rule of engineering – do not consider complex versions of the problem until the simple versions have been solved – and in part due to oversight of another such rule – if the artifact you are trying to build is made up of several parts, the construction process should understand what such elementary parts are and how they come together. The present paper explores an evolutionary solution to the task of building a story that combines more than one plot line into a single linear discourse. This requires a set of knowledge resources that capture the main features that influence the decisions involved – namely a set of basic plot lines as sequences of scenes, each annotated with the characters that take part, the narrative roles they play, and basic semantics such as when characters are born, die, or fall in love. A representation suitable for evolutionary treatment is proposed for discourses with several plot lines, and a set of fitness functions are defined based on metrics related to the quality of the resulting discourses are proposed. The solution defined over these elements produces populations of stories with elaborate discourses that combine several subplots.

The combination of several plot lines into a discourse is more complex than a simple weaving. Plot lines are not actually independent streams of narrative discourse that get combined together into a complex fabric: the character sets from different subplots combined into a story do not remain distinct, they may be merged so that the same character in the overall story often plays different roles in more than one of the subplots. This point is addressed explicitly in the solution proposed in this paper. The process we want to model involves an additional operation of merging (some of the characters in) the narrative threads for the different plotlines by instantiating their narrative roles (either main or secondary) with the set of characters for the overall plot.

## 2 Related Work

Three topics are considered relevant for this paper: prior solutions for plot line combination, quantitative metrics for stories, and evolutionary approaches to creation of narratives of some kind.

### 2.1 Plot Line Combination

In recent years there has been an increase in the number of research efforts that consider the construction of stories with more than one plot line. In reviewing research efforts on this topic, we have opted for unifying the terminology under an abstract concept of _plot line_ considered as a sequence of plot-relevant elements that make sense in the order in which they appear in the story, and linked by at least a shared set of protagonist and secondary characters. We will refer to the plot-relevant elements in a plot line as _scenes_. When more than one plot line are involved in a larger story, each of these plot lines is considered a _subplot_ of the story.

Two different approaches have been followed to create multi-plotline stories. In the first one, the story is created by adding scenes incrementally, switching between different plot lines so that each of the plot lines involved is also dynamically constructed. In the second one, a set of existing plot lines is considered at the start, and the construction process involves deciding how these plot lines will be combined in the discourse for the final story.

Under the first approach, Porteous et al. \[[16](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR16 "Porteous, J., Charles, F., Cavazza, M.: Plan-based narrative generation with coordinated subplots. In: European Conference on Artificial Intelligence (ECAI 2016), vol. 285, pp. 846–854. IOS Press (2016)")\] describe an interactive storytelling system that builds stories in a way that the resulting story will show multiple interleaved plot lines. Their system relies on a plan-based approach that takes input parameters that govern the number of plot lines that should be involved in the final version and how much of the final story should taken up by each plot line.

Under the second approach, systems first compile a set of narrative threads from a given source and then search for possible combinations of them that make a story. Fay \[[3](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR3 "Fay, M.P.: Driving story generation with learnable character models. Ph.D. thesis, Massachusetts Institute of Technology (2014)")\] constructs multi-plotline stories by combining together narrative threads for specific types of characters found in a given story request, so that main characters in the story request are bound to secondary characters in threads for other characters and the elements from each thread are combined into a consistent overall timeline. The Raconteur \[[6](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR6 "Gervás, P.: Composing narrative discourse for stories of many characters: a case study over a chess game. Literary Linguist. Comput. 29(4), 511–531 (2014)")\] and StoryFire \[[5](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR5 "Gervás, P.: Storifying observed events: could i dress this up as a story? In: 5th AISB Symposium on Computational Creativity. AISB, AISB, University of Liverpool, UK, April 2018")\] systems obtain narrative threads from a conceptual description of a chess-game, and builds stories by selecting a _plot schema_ to use as a template to be filled in with matching scenes from the available threads. The PlotAssembler system \[[7](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR7 "Gervás, P.: Generating a search space of acceptable narrative plots. In: 10th International Conference on Computational Creativity (ICCC 2019). UNC Charlotte, North Carolina, USA, July 2019")\] builds stories by combining a set of small spans of narrative discourse called _axes of interest_ in ways that interweave their scenes, ensuring that character continuity across scenes is compatible with probabilities mined from a corpus of prior stories. The work of Concepción et al. \[[2](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR2 "Concepción, E., Gervás, P., Méndez, G.: Exploring baselines for combining full plots into multiple-plot stories. New Generation Computing 38(4), 593–633 (2020). 
https://doi.org/10.1007/s00354-020-00115-x
")\] explores baseline solutions for weaving together a set of plot lines into stories. The plot lines considered include additional information on roles played by the characters. The set of weaving procedures includes some based on existing literary techniques and some presented as baselines for computational approaches to the task.

### 2.2 Computational Metrics for Stories

Over the past few years a body of computational metrics for stories has been developed. As the set of features that might be considered in a story is vast, these metrics generally focus on particular aspects that are relevant for specific purposes. When the goal is to invent a new story, metrics relevant to the purpose focus on aspects that may be related to originality: story novelty \[[14](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR14 "Peinado, F., Francisco, V., Hervás, R., Gervás, P.: Assessing the novelty of computer-generated narratives using empirical metrics. Minds Mach. 20(4), 588 (2010). 
https://doi.org/10.1007/s11023-010-9209-8
")\], similarity between stories \[[9](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR9 "Hervás, R., Sánchez-Ruiz, A.A., Gervás, P., León, C.: Calibrating a metric for similarity of stories against human judgement. In: ICCBR (Workshops), pp. 136–145 (2015)")\] and correlations between easy-to-measure features in the stories and the creativity attributed to them by human judges \[[20](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR20 "Tapscott, A., Gomez, J., León, C., Smailovic, J., Znidarsic, M., Gervás, P.: Empirical evidence of the limits of automatic assessment of fictional ideation. In: C3GI ESSLLI (2016)")\].

More recent work addresses the evaluation of multi-plotline stories specifically. An attempt at formative qualitative evaluation of multi-plotline stories was carried out in \[[2](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR2 "Concepción, E., Gervás, P., Méndez, G.: Exploring baselines for combining full plots into multiple-plot stories. New Generation Computing 38(4), 593–633 (2020). 
https://doi.org/10.1007/s00354-020-00115-x
")\]. A group of human judges were asked to consider the quality of 10 examples of multi-plotline stories, and to identify specific features that they considered positive or negative contributions to the perceived value of the story. A number of interesting conclusions were drawn. First, the most detrimental feature to perceived story quality was the existence of semantic inconsistencies in the story, such as characters that keep taking part in the story after being dead. Second, positive judgments often involved identification of characteristics of the story that were optional rather than necessary, such as the existence of an overarching plot, or the fact that one subplot was inserted fully within another. In \[[8](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR8 "Gervás, P., Concepción, E., Méndez, G.: Assessing multiplot stories: from formative analysis to computational metrics. In: 12th International Conference on Computational Creativity (ICCC 2019), Mexico City, Mexico, September 2021")\], the qualitative analyses presented as part of the formative evaluation were distilled into a set of metrics designed to capture them in a numerical form. These metrics were designed to respond to the set of features that human judges were seen to focus on when asked to assess multi-plotline stories, and to translate the judgments made onto numerical scores.

### 2.3 Evolutionary Construction of Narratives

Without pretending to be exhaustive, this section reviews some of the existing efforts to generate narratives by means of evolutionary solutions in terms of two different aspects: which elements they combine and what type of fitness function they employ.

In terms of the elements that are combined to make stories, McIntyre and Lapata \[[13](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR13 "McIntyre, N., Lapata, M.: Plot induction and evolutionary search for story generation. In: Proceedings of the 48th Annual Meeting of the Association for Computational Linguistics, pp. 1562–1572. Association for Computational Linguistics, Uppsala, Sweden, July 2010. 
https://aclanthology.org/P10-1158
")\] present a plot generator that builds a plot from the set of entities appearing in a sentence provided by the user. For each entity in the sentence the system retrieves a plot line from a knowledge based automatically extracted previously, and creates a space of possible stories involving the given entities by merging together these plot lines. This search space is then explored by means of genetic algorithms, using as fitness function a combination of story coherence and story interest. Gómez de Silva and Pérez y Pérez \[[19](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR19 "de Silva Garza, A.G., y Pérez, R.P.: Towards evolutionary story generation. In: Colton, S., Ventura, D., Lavrac, N., Cook, M. (eds.) Proceedings of the Fifth International Conference on Computational Creativity, ICCC 2014, Ljubljana, Slovenia, 10–13 June 2014, pp. 332–335. computationalcreativity.net (2014). 
http://computationalcreativity.net/iccc2014/wp-content/uploads/2014/06/15.3_Garza.pdf
")\] propose a model of story construction that combines the MEXICA existing knowledge-based story generator \[[15](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR15 "Pérez y Pérez, R., Sharples, M.: Mexica: a computer model of a cognitive account of creative writing. J. Exp. Theor. Artif. Intell. 13(2), 119–139 (2001)")\] with the GENCAD evolutionary approach for the adaptation stage in case-based solutions to architectural problems \[[18](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR18 "Gómez de Silva Garza, A.: An evolutionary approach to design case adaptation. Ph.D. thesis, The University of Sydney, Australia (2000)")\]. The story construction model relies on the knowledge-based heuristics of MEXICA to build initial populations and applies the evolutionary approach to refine them. Among the features that the fitness functions are designed to detect are individuals with ‘incestuous ancestry’, built by applying more than once rules from the same exemplar, which may lead to repetition of events in the output story.

In terms of the fitness functions employed to drive the evolutionary approach, Fredericks and DeVries \[[4](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR4 "Fredericks, E.M., DeVries, B.: (Genetically) improving novelty in procedural story generation. arXiv preprint 
arXiv:2103.06935
(2021)")\] describe an application of an evolutionary solution driven by novelty search \[[11](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR11 "Lehman, J., Stanley, K.O.: Exploiting open-endedness to solve problems through the search for novelty. In: Proceedings of the Eleventh International Conference on Artificial Life. MIT Press (2004)")\] to improve the novelty of procedurally-generated small narratives fragments for text-based games. Kartal et al. \[[10](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR10 "Kartal, B., Koenig, J., Guy, S.J.: User-driven narrative variation in large story domains using Monte Carlo tree search. In: Proceedings of the 2014 International Conference on Autonomous Agents and Multi-agent Systems, AAMAS 2014, pp. 69–76. International Foundation for Autonomous Agents and Multiagent Systems, Richland, SC (2014)")\] use Monte Carlo tree search to drive planning-based narrative generation in support of a interactive framework for user-driven narrative variation. They rely for selection on a combination of the believability of the resulting story and the percentage of the user-defined goals the current story accomplishes. Soares de Lima et al. \[[12](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR12 "de Lima, E.S., Feijó, B., Furtado, A.L.: Procedural generation of quests for games using genetic algorithms and automated planning. In: 18th Brazilian Symposium on Computer Games and Digital Entertainment, SBGames 2019, Rio de Janeiro, Brazil, 28–31 October 2019, pp. 144–153. IEEE (2019). 
https://doi.org/10.1109/SBGames.2019.00028
")\] combine planning with an evolutionary search strategy guided by story arcs to generate quests for games. Candidate quests are constructed by a planner as linear sequences of events or tasks to be accomplished by the player. The evolutionary algorithm chooses among them using a fitness function that builds for each candidate quest the sequence of tensions that arise from it, and scores it based on its match with a target curve of evolving tensions provided by the user.

## 3 An Evolutionary Multiplot Story Composer

A story built by combining plot lines requires a complex set of decisions: in which order to combine the scenes from the different plot lines and how to merge the characters sets from the different plot lines into a single set of characters for the overall story. The search space of possible solutions is immense. Prior attempts to explore this search space in terms of heuristics for informing the required decisions \[[2](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR2 "Concepción, E., Gervás, P., Méndez, G.: Exploring baselines for combining full plots into multiple-plot stories. New Generation Computing 38(4), 593–633 (2020). 
https://doi.org/10.1007/s00354-020-00115-x
")\] have shown that stories produced in this way are significantly more rigid in structure than human produced stories. An evolutionary solution based on fitness functions that capture some of the desired features for the output stories may provide efficient means of traversing this search space.

### 3.1 The Knowledge Resources

The experiments reported in this paper are carried out over a set of plot lines extracted from a compilation of classic plots used in cinema \[[1](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR1 "Balló, J., Pérez, X.: La semilla inmortal: los argumentos universales en el cine. Ed. Anagrama, Barcelona (2007)")\]. A subset of these plots have been distilled into a set of _plot templates_, which are formalised knowledge resources that describe the structure of the plot as a sequence of scenes. The set of plot templates currently available is: The Benevolent Outsider, The Creation of Artificial Life, Descent into the Underworld, The Destructive Outsider, Faust, Split Person Comic, Split Person Tragic.

Each _scene_ describes the characters that take part, the narrative roles they play, the set of semantic annotations that are used by the system to check consistency, and a template for rendering the scene as text. The narrative roles played by the characters are represented by labels that identify the main characters involved in a given plot – say, Creator and Creature in a Creation of Artificial Life plot, or Tempter and Tempted in a Faust plot. The semantic annotations cover aspects about the meaning of the scene that may affect the perceived consistency of the stories in which they appear. The current version considers the following semantic annotations: whether characters are _created/born or die_ in the scene and whether characters _fall in love or out of love_. These semantic annotations allow the definition of metrics to identify situations where narrative roles from different subplots are assigned to the same character in the story, and events affecting the different roles are incompatible – characters dying more than once, or serially falling in love. These metrics are used to inform the fitness function for the evolutionary solution.

Each plot template has a particular character identified as the _protagonist_ – this is usually one of the characters playing an important role in the plot.

This set of features emerges from the analysis of a number of multi-plot stories described in \[[2](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR2 "Concepción, E., Gervás, P., Méndez, G.: Exploring baselines for combining full plots into multiple-plot stories. New Generation Computing 38(4), 593–633 (2020). 
https://doi.org/10.1007/s00354-020-00115-x
")\] and the metrics for automated assessment of quality of multi-plotline stories presented in \[[8](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR8 "Gervás, P., Concepción, E., Méndez, G.: Assessing multiplot stories: from formative analysis to computational metrics. In: 12th International Conference on Computational Creativity (ICCC 2019), Mexico City, Mexico, September 2021")\]. The insights from these analyses have identified these features as relevant to the perception of quality of a multi-plotline story.

### 3.2 Character Fusion and Discourse Planning

The analyses carried out to this point on how multi-plotline stories are put together show that, given a set of subplots to be considered as inputs, there are two different processes that contribute to the final result.

The first process is related to the set of characters that take part in each subplot. For a story to be successful, it appears to be important that the sets of characters involved in each subplot have a non-empty intersection. In operational terms, this is achieved by unifying some character _a_ from subplot _A_ with character _b_ from another subplot _B_, so that a single character – say _John_ – in the story undertakes both the part of character _a_ from subplot _A_ and the part of character _b_ from subplot _B_. We refer to this operation as _character fusion_. In terms of traditional views on natural language generation \[[17](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR17 "Reiter, E., Dale, R.: Building Natural Language Generation Systems. Cambridge University Press, Cambridge (2000)")\] this operation is a part of the task of _content determination_, since the nature of subplots is somewhat changed in the process of attributing particular characters to the variables in the corresponding template.

The second process is related to the order in which the scenes from the different subplots are presented in the discourse for the final story. This is known to be crucial to the impact that the story has on the audience, and exploited intentionally by authors to achieve effects such as _suspense_ – where presentation of certain information is withheld on purpose – or _cliff-hanger breaks_ – where transitions to cover other subplots are made at points where tension is high in the current subplot. In terms of traditional views on natural language generation \[[17](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR17 "Reiter, E., Dale, R.: Building Natural Language Generation Systems. Cambridge University Press, Cambridge (2000)")\] this operation is a fundamental part of the task of _discourse planning_.

Character fusion and discourse planning are tightly interconnected by the information in the semantic annotations for scenes. A fusion between a character _a_ from one template _A_ and a character _b_ from another template _B_ is only possible if it will not result in a final discourse in which the fused character is seen to behave in an impossible manner – such as being born or dying more than once, or being involved in more than one passionate romance without the fact being addressed by the story.[Footnote 1](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Fn1) The metrics that inform the fitness function should penalise the scores of stories that incur in this type of inconsistency. Even if none of these extreme inconsistencies occur, a particular discourse plan may be incoherent if a fused character takes part in events that happen in the final discourse either before its birth or after its death. Specific metrics for identifying these situations are also needed.

### 3.3 Representing Multiplot Stories for Evolutionary Construction

In order to apply an evolutionary approach, each story draft needs to be represented in terms of some kind of genetic information that describes how it addresses the main tasks involved: discourse planning and character fusion. To achieve this we propose a solution in several parts.

The problem of constructing a multiplot line story considers the following inputs: a set of plot lines to combine, where each plot line is defined by a narrative thread expressed as a sequence of scenes together with a set of characters that appear in it.

This implies that, for a particular problem of combining N plotlines, the length of the final discourse is determined by the total number of scenes in the narrative threads being considered, and the maximum number of possible characters featuring in the story is determined by the union of the sets of characters in the narrative threads being considered.

For simplicity, we are assuming that the relative chronological order of the scenes in each narrative thread is respected in the final discourse. This is not a necessary condition. Indeed, many stories present instances of altered chronology (flashbacks, flashforwards). However, we leave this point to be addressed in further work.

The characterisation of the discourse plan for a given story candidate requires: establishing which narrative thread to start on, defining the specific points in the final sequence in which the discourse switches to a different narrative thread, and defining to which of the other available threads the discourse is switching when it does.

The representation is based on the fact that, for a given story construction problem, the length of the final discourse is known and fixed, and the fact that the set of plotlines being considered is known and fixed.

The information on discourse planning is represented in terms of vectors that define how the narrative threads for the different plot lines are combined into the final linear discourse:

-   a single digit (0 or 1) defines which narrative thread the final discourse starts with
    
-   a sequence of digits (0 or 1) defines for the total number of scenes in the final discourse whether the next scene follows on with the prior narrative thread or it switches to a different thread
    
-   a sequence of digits (ranging between 1 and N − 1, where N is the total number of plots being combined) defines how many of the available plots are skipped whenever the discourse switches to a different narrative thread
    

The set of possible characters for the complete story is defined by the union of the sets of variable names for the characters appearing in each narrative thread. These variable names need to be distinct across the different narrative threads to avoid confusion. This is ensured by assigning a prefix with the plotline name to all the variable names that feature in any given narrative thread.

The caracterisation of the choices for character fusion for a given story candidate requires an assignment of character names to each of the variables in the joint set of variables for the story.

For simplicity, the set of potential character names for the story is defined to be the set of integers from 0 to C, with C being the cardinality of the joint set of variables for the story. This is sufficient to represent any choices made in terms of character fusion (with variables in two different positions in the name-assignment vector being assigned to the same integer). The form of the resulting stories would be significantly improved by a later stage of transforming these integer names for the characters into strings representing realistic names.

An example of representation is shown in Fig. [1](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Fig1).

**Fig. 1.**

[![figure 1](https://media.springernature.com/lw685/springer-static/image/chp%3A10.1007%2F978-3-031-03789-4_5/MediaObjects/529045_1_En_5_Fig1_HTML.png)](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5/figures/1)

Genetic representation for a combination of three plots of length 5, each with 3 characters. Fuses characters B (p0)/E (p1), C (p0)/G (p2) and D (p1)/I (p2).

[Full size image](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5/figures/1)

### 3.4 Constructing an Initial Population

An initial population of story candidates is built by assigning values to the representation described in Sect. [3.3](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Sec9). For each of the different parts of the representation the process of assignment of values needs to be treated differently.

For the initial digit that defines which narrative thread to start on, and for the vector of decisions on whether to switch, random choice between 0 and 1 is suitable.

For the vector of decisions on skip size at each switch, random choice between 1 and N − 1 (with N the total number of plots being combined) is suitable.

For the vector of decisions of which character to assign to each variable, the choice is more complex. This is because variables from the same narrative thread should not be assigned to the same character, at the risk of confusing the relations between characters in the corresponding subplot. The process of assignment is carried out separately for the set of variables for each thread. For such a set of variables, the process decides at random whether to assign to each variable either a character name chosen at random from those already used in some of the narrative threads already processed, or an entirely new character name chosen at random from the character names that remain free. This ensures the required constraints are satisfied.

### 3.5 Evolutionary Operators

Once a population has been constructed, mutation and cross over operators are applied to it.

Because of the different nature of the various parts of the representation, specific operators of each kind are applied to the different parts.

For the mutation operators:

-   for the starting point gene, the value is mutated at random
    
-   for the switch point vector, values at each point are either mutated or not depending on a threshold parameter
    
-   for the skip size vector, values at each point are either mutated or not depending on a threshold parameter, and, if required, mutated to a value chosen at random within the required range
    
-   for the character assignment vector, character names at each point are either mutated or not depending on a threshold parameter, and, if required, mutated to a character name chosen at random within the required range
    

For the cross over operators:

-   for the starting point gene, the value of the two individuals being considered is swapped
    
-   for the switch point vector, a point in the vector is chosen at random and the corresponding halves of the vectors for the two individuals are swapped over
    
-   for the skip size vector, a point in the vector is chosen at random and the corresponding halves of the vectors for the two individuals are swapped over
    
-   for the character assignment vector, the assignments of characters for the two different individuals are swapped over
    

### 3.6 Fitness Functions

The construction of potential story drafts as described in the initialisation of the population and the evolutionary operators is mostly random. However not all possible combinations are actually valid. Certain plot lines, when combined in certain orders, give rise to incoherence in the semantics of the story. Incoherence may affect different aspects: characters that act before being born or after being dead, or characters that fall in love serially with no regard for previous romances. It falls to the fitness function to differentiate between valid and invalid story candidates. This is achieved by taking into account the knowledge resources described in Sect. [3.1](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Sec7).

As there are many different aspects to be considered for a story, a modular approach is applied to the definition of a fitness function for the system. Rather than build a complex fitness function that addresses all the aspects, a number of targeted fitness functions are built, and the fitness for a given individual is computed as a function of the results it achieves under the specific fitness functions.

This approach allows a differentiated consideration of the aspects related to validity of the story draft, the aspects related to satisfaction of optional traits, and the aspects that may actually relate to perceived quality of any given solution.

The different aspects that need to be considered as contributing to the quality of stories differ in the way they impact the overall perception of a reader. These different ways require different solutions to model numerically the expected behaviour. The solution presented here is a tentative proposal that captures the basic intuitions arising from prior empirical studies. Further work may need more detailed empirical studies and matching adaptations of the computational solutions.

**Validity Fitness Functions.** A first set of fitness functions addresses the consistency of the final discourse in terms of the semantics for the scenes as annotated in the knowledge resources described in Sect. [3.1](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Sec7). All these functions assign a score of 100 if the story is consistent with respect to the corresponding feature, and 0 otherwise.

The current set of fitness functions includes the following aspects that affect the validity of a story draft:

-   whether characters are born more than once in the story (rules out combinations of plot lines that merge into a character two subplots that both mention the birth)
    
-   whether characters die more than once in the story (rules out combinations of plot lines that merge into a character two subplots that both mention the death)
    
-   whether characters are active in the story at points that do not lie between their birth and their death (or the boundaries of the story if birth or death are not mentioned)
    
-   whether the romantic behaviour of characters is consistent (rules out combinations of subplots that imply one character is passionately in love with different people)
    

The fitness function for consistent romantic behaviour is currently an initial approximation to the task. Cases where characters fall in love with more than one person do exist as valid stories, but they are only interesting when the plot addresses the romantic conflict explicitly and resolves it in some way. The limited procedure of story construction applied here – restricted to interweaving scenes from two different plots – cannot address this task in its current form. Further work will consider extensions to the construction procedure and a matching revised fitness function to address this issue.

**Optional Traits Fitness Functions.** The second set of fitness functions addresses aspects noted to be positive traits by the human judges but which constitute optional rather than necessary configurations for a story. These traits add value to a story when present but do not detract from its quality if absent.

Fitness functions are defined to capture the corresponding traits, also scoring 100 if the trait is present and 0 if it is absent.

In the present version of the system, such fitness functions are added to the mix for a given run only if the corresponding trait is desired in the outcome population.

The following traits are considered for discourse plans:

-   _inserted subplot_: a complete subplot is inserted as an aside into the story (all scenes from the subplot appear together in the final discourse, and surrounded by scenes from other subplots)
    
-   _overarching plot_: the story starts and finishes with scenes from the same subplot, which therefore appears as a frame for any other subplots in the story – this does occur in cases where there is an inserted subplot but may also occur in other situations, and therefore it is considered as a separate feature
    

Additional traits may be considered in the same way for character fusions, which establish a link between the casts of the subplots involved in any given story. The importance of the link depends on the relative importance of the character involved in the link with respect to each of the subplots. For the present paper, the following type of links have been considered:

-   _shared protagonist_: the same character acts as protagonist of two subplots
    
-   _stitching protagonist_: the protagonist from one subplot plays an important role – different from the corresponding protagonist – in another
    

Fitness functions of the type explained above are defined for each of these types of links, allowing the outcomes to be driven towards stories satisfying the corresponding criteria.

**Combining Fitness Functions to Score Individual Stories.** To ensure that the different types of fitness functions described above are combined into a single score for each candidate story in a population, stories are assigned as a final score the average of the scores for the set of fitness functions for specific features selected.

This ensures that individual stories that are invalid or do not exhibit the desired traits disappear from the population as early as possible, and that stories with higher quality have a higher chance of survival.

## 4 Discussion

The results of the proposed system are presented and the relation of the proposed approach with previous work is discussed.

### 4.1 Results

The proposed system is run in each case with an initial population of 1,000 individuals generated at random, with the described operators for mutation (probability of mutation set to 0.2) and crossover (probability of cross over set to 0.05), for 20 generations. At each generation populations are culled by selecting the next generation using a best scoring criterion.

**Table 1. An example of output story combining the plotlines creation of artificial life (CLM) and split person tragic (SPT). Columns show: the _text_ for the story broken down by scenes, description of the _discourse plan_ indicating for each scene which plotline it comes from, description of the cast indicating the roles they play in the respective plot lines and what names have been assigned to them – which reflect any _character fusions_ present. Columns 1 and 2 are aligned by scenes, column 3 applies to the story as a whole.**

[Full size table](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5/tables/1)

Some examples of results are shown below.

The stories generated by the system are rendered as text using the templates stored for the corresponding scenes in the knowledge resources, replacing the variables with the assigned character names. An example of complete story is shown in Table [1](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Tab1). Numbers used internally as character names have been replaced with capital letters for ease of reading. This story is obtained with the configuration set to construct stories with an inserted plot. The discourse plan indeed shows all scenes from CLM plot appearing together, bracketted by scenes from SPT. In this case, the two subplots are only very lightly connected by character fusions: variable CLM-0, the protagonist of CLM, playing the role of Frankenstein has been fused with variable SPT-2 that corresponds to a secondary character in SPT.

**Table 2. Structures for stories obtained with different configurations for the optional traits concerning discourse structure, using different combinations of plotlines creation of artificial life (CLM), split person tragic (SPT), Faust (FA) and descent into the underworld (DiU). Column 1 shows a story with inserted plots, column 2 shows a story with overarching plot but no inserted plot, column 3 shows a story with neither overarching plot nor inserted plot. For ease of understanding of the structure of the discourse plans, the scenes of one of the subplots are highlighted in bold.**

[Full size table](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5/tables/2)

To illustrate the operation of the fitness functions for optional traits, examples of the structure of different stories are shown in Table [2](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Tab2).

**Table 3. Examples to illustrate options on character fusion. Names of fused characters are highlighted in bold.**

[Full size table](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5/tables/3)

To illustrate the operation of the fitness functions for character fusion, examples of different stories are shown in Table [3](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Tab3). To provide informative views while respecting page limit constraints, only cast descriptions are shown. The first column is an example of shared protagonist (same character A plays Orpheus and Faust). The second column is an example of stitching protagonist (character A plays Orpheus and Mephistopheles and character B plays Euridice and Faust). The third column is a weaker example of stitching protagonist (character C plays Hades and Faust).

### 4.2 Relation with Previous Work

The character fusion operation considered here is comparable to binding between characters as used by Fay \[[3](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR3 "Fay, M.P.: Driving story generation with learnable character models. Ph.D. thesis, Massachusetts Institute of Technology (2014)")\].

The procedure applied in McIntyre and Lapata \[[13](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR13 "McIntyre, N., Lapata, M.: Plot induction and evolutionary search for story generation. In: Proceedings of the 48th Annual Meeting of the Association for Computational Linguistics, pp. 1562–1572. Association for Computational Linguistics, Uppsala, Sweden, July 2010. 
https://aclanthology.org/P10-1158
")\] shows significant parallels with our own approach: a set of possible stories is created by combining plot lines from different stories and then an evolutionary approach is applied to search for a convincing set of output stories. However, our system differs in that it takes as input a set of already established plot lines that cannot be altered, whereas McIntyre and Lapata explore different choices of elements – tree structures corresponding to sentences – to build the stories.

The metric for detecting individuals with ‘incestuous ancestry’ in \[[19](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR19 "de Silva Garza, A.G., y Pérez, R.P.: Towards evolutionary story generation. In: Colton, S., Ventura, D., Lavrac, N., Cook, M. (eds.) Proceedings of the Fifth International Conference on Computational Creativity, ICCC 2014, Ljubljana, Slovenia, 10–13 June 2014, pp. 332–335. computationalcreativity.net (2014). 
http://computationalcreativity.net/iccc2014/wp-content/uploads/2014/06/15.3_Garza.pdf
")\], intended as it is to avoid repetition of events in the stories, is related to our fitness function to avoid characters in the stories falling in love more than once. Attempts to combine more than two plotlines may require a similar adaptation to avoid, at least initially, stories that include the same plot line several times.

The semantic annotations for the plot templates in our knowledge resources play a similar role to the domain database as considered in \[[12](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR12 "de Lima, E.S., Feijó, B., Furtado, A.L.: Procedural generation of quests for games using genetic algorithms and automated planning. In: 18th Brazilian Symposium on Computer Games and Digital Entertainment, SBGames 2019, Rio de Janeiro, Brazil, 28–31 October 2019, pp. 144–153. IEEE (2019). 
https://doi.org/10.1109/SBGames.2019.00028
")\] to compute tension. The judgement on validity of stories based on these semantic annotations plays a role similar to the believability metric as considered in \[[10](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR10 "Kartal, B., Koenig, J., Guy, S.J.: User-driven narrative variation in large story domains using Monte Carlo tree search. In: Proceedings of the 2014 International Conference on Autonomous Agents and Multi-agent Systems, AAMAS 2014, pp. 69–76. International Foundation for Autonomous Agents and Multiagent Systems, Richland, SC (2014)")\].

## 5 Conclusions

The evolutionary approach to constructing multi-plotline stories provides efficient means of building a population of drafts that satisfy constraints on semantic validity over the final linear discourse for the story. The drafts in the population can be steered towards stories that satisfy specific features in terms of particular structures in the discourse plan (such as overaching plot or inserted plots) and/or particular choices for character fusion (such as shared protagonists, linking roles or only loose connections between the casts of the different subplots).

The current set of features identified as relevant to story quality is not well suited to numerical ranking in terms of fitness functions. As a result, final populations tend to converge towards scores of 100/100 for all individuals. Nevertheless, the fact that scores for individuals are constructed as a combination of more specific scores for particular features implies that during the construction procedure – in earlier generations of the evolution – individuals do have scores in the range between 0 and 100. This allows the evolutionary procedure to explore different combinations of the various subparts of the representation vector, to achieve a set of valid solutions in the final population that satisfy the desired constraints.

As future work we will consider extending our system with metrics of the various types used in the other approaches reviewed: believability, story arcs based on tension.

Although user-defined goals are a feature specific to user-driven narratives of the type addressed in \[[4](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR4 "Fredericks, E.M., DeVries, B.: (Genetically) improving novelty in procedural story generation. arXiv preprint 
arXiv:2103.06935
(2021)")\] and \[[10](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR10 "Kartal, B., Koenig, J., Guy, S.J.: User-driven narrative variation in large story domains using Monte Carlo tree search. In: Proceedings of the 2014 International Conference on Autonomous Agents and Multi-agent Systems, AAMAS 2014, pp. 69–76. International Foundation for Autonomous Agents and Multiagent Systems, Richland, SC (2014)")\], stories built outside these contexts often do have a purpose beyond entertainment – convincing, educating,...Moreover, there may not be a single goal but rather a set of goals to achieve. Under this light, extending the fitness functions for our system with metrics for percentage of goals achieved will be considered as future work.

It seems that evolutionary approaches have been used often for story generation as a secondary process applied to a set of stories constructed previously by some other method. Examples of this initial material produced by other means are the stories built by MEXICA in \[[19](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR19 "de Silva Garza, A.G., y Pérez, R.P.: Towards evolutionary story generation. In: Colton, S., Ventura, D., Lavrac, N., Cook, M. (eds.) Proceedings of the Fifth International Conference on Computational Creativity, ICCC 2014, Ljubljana, Slovenia, 10–13 June 2014, pp. 332–335. computationalcreativity.net (2014). 
http://computationalcreativity.net/iccc2014/wp-content/uploads/2014/06/15.3_Garza.pdf
")\] and the grammar-driven quest sketches produced by Tracery in \[[4](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#ref-CR4 "Fredericks, E.M., DeVries, B.: (Genetically) improving novelty in procedural story generation. arXiv preprint 
arXiv:2103.06935
(2021)")\]. In our case, we apply the evolutionary solution to combine plot templates that constitute already-built stories. The solution we propose could be used in future work as a secondary process on the results of preceding story generation procedures of a different type.

## Notes

1.  1.
    
    For clarifications on how romantic conflicts are handled in the current version of the system see the discussion in Sect. [3.6](https://link.springer.com/chapter/10.1007/978-3-031-03789-4_5#Sec12).
    

## References

1.  Balló, J., Pérez, X.: La semilla inmortal: los argumentos universales en el cine. Ed. Anagrama, Barcelona (2007)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Ball%C3%B3%2C%20J.%2C%20P%C3%A9rez%2C%20X.%3A%20La%20semilla%20inmortal%3A%20los%20argumentos%20universales%20en%20el%20cine.%20Ed.%20Anagrama%2C%20Barcelona%20%282007%29) 
    
2.  Concepción, E., Gervás, P., Méndez, G.: Exploring baselines for combining full plots into multiple-plot stories. New Generation Computing **38**(4), 593–633 (2020). [https://doi.org/10.1007/s00354-020-00115-x](https://doi.org/10.1007/s00354-020-00115-x)
    
    [CrossRef](https://doi.org/10.1007%2Fs00354-020-00115-x)  [Google Scholar](https://scholar.google.com/scholar_lookup?&title=Exploring%20baselines%20for%20combining%20full%20plots%20into%20multiple-plot%20stories&journal=New%20Generation%20Computing&doi=10.1007%2Fs00354-020-00115-x&volume=38&issue=4&pages=593-633&publication_year=2020&author=Concepci%C3%B3n%2CE&author=Gerv%C3%A1s%2CP&author=M%C3%A9ndez%2CG) 
    
3.  Fay, M.P.: Driving story generation with learnable character models. Ph.D. thesis, Massachusetts Institute of Technology (2014)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Fay%2C%20M.P.%3A%20Driving%20story%20generation%20with%20learnable%20character%20models.%20Ph.D.%20thesis%2C%20Massachusetts%20Institute%20of%20Technology%20%282014%29) 
    
4.  Fredericks, E.M., DeVries, B.: (Genetically) improving novelty in procedural story generation. arXiv preprint [arXiv:2103.06935](http://arxiv.org/abs/2103.06935) (2021)
    
5.  Gervás, P.: Storifying observed events: could i dress this up as a story? In: 5th AISB Symposium on Computational Creativity. AISB, AISB, University of Liverpool, UK, April 2018
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Gerv%C3%A1s%2C%20P.%3A%20Storifying%20observed%20events%3A%20could%20i%20dress%20this%20up%20as%20a%20story%3F%20In%3A%205th%20AISB%20Symposium%20on%20Computational%20Creativity.%20AISB%2C%20AISB%2C%20University%20of%20Liverpool%2C%20UK%2C%20April%202018) 
    
6.  Gervás, P.: Composing narrative discourse for stories of many characters: a case study over a chess game. Literary Linguist. Comput. **29**(4), 511–531 (2014)
    
    [MathSciNet](http://www.ams.org/mathscinet-getitem?mr=3138890)  [CrossRef](https://doi.org/10.1093%2Fllc%2Ffqu040)  [Google Scholar](https://scholar.google.com/scholar_lookup?&title=Composing%20narrative%20discourse%20for%20stories%20of%20many%20characters%3A%20a%20case%20study%20over%20a%20chess%20game&journal=Literary%20Linguist.%20Comput.&volume=29&issue=4&pages=511-531&publication_year=2014&author=Gerv%C3%A1s%2CP) 
    
7.  Gervás, P.: Generating a search space of acceptable narrative plots. In: 10th International Conference on Computational Creativity (ICCC 2019). UNC Charlotte, North Carolina, USA, July 2019
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Gerv%C3%A1s%2C%20P.%3A%20Generating%20a%20search%20space%20of%20acceptable%20narrative%20plots.%20In%3A%2010th%20International%20Conference%20on%20Computational%20Creativity%20%28ICCC%202019%29.%20UNC%20Charlotte%2C%20North%20Carolina%2C%20USA%2C%20July%202019) 
    
8.  Gervás, P., Concepción, E., Méndez, G.: Assessing multiplot stories: from formative analysis to computational metrics. In: 12th International Conference on Computational Creativity (ICCC 2019), Mexico City, Mexico, September 2021
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Gerv%C3%A1s%2C%20P.%2C%20Concepci%C3%B3n%2C%20E.%2C%20M%C3%A9ndez%2C%20G.%3A%20Assessing%20multiplot%20stories%3A%20from%20formative%20analysis%20to%20computational%20metrics.%20In%3A%2012th%20International%20Conference%20on%20Computational%20Creativity%20%28ICCC%202019%29%2C%20Mexico%20City%2C%20Mexico%2C%20September%202021) 
    
9.  Hervás, R., Sánchez-Ruiz, A.A., Gervás, P., León, C.: Calibrating a metric for similarity of stories against human judgement. In: ICCBR (Workshops), pp. 136–145 (2015)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Herv%C3%A1s%2C%20R.%2C%20S%C3%A1nchez-Ruiz%2C%20A.A.%2C%20Gerv%C3%A1s%2C%20P.%2C%20Le%C3%B3n%2C%20C.%3A%20Calibrating%20a%20metric%20for%20similarity%20of%20stories%20against%20human%20judgement.%20In%3A%20ICCBR%20%28Workshops%29%2C%20pp.%20136%E2%80%93145%20%282015%29) 
    
10.  Kartal, B., Koenig, J., Guy, S.J.: User-driven narrative variation in large story domains using Monte Carlo tree search. In: Proceedings of the 2014 International Conference on Autonomous Agents and Multi-agent Systems, AAMAS 2014, pp. 69–76. International Foundation for Autonomous Agents and Multiagent Systems, Richland, SC (2014)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Kartal%2C%20B.%2C%20Koenig%2C%20J.%2C%20Guy%2C%20S.J.%3A%20User-driven%20narrative%20variation%20in%20large%20story%20domains%20using%20Monte%20Carlo%20tree%20search.%20In%3A%20Proceedings%20of%20the%202014%20International%20Conference%20on%20Autonomous%20Agents%20and%20Multi-agent%20Systems%2C%20AAMAS%202014%2C%20pp.%2069%E2%80%9376.%20International%20Foundation%20for%20Autonomous%20Agents%20and%20Multiagent%20Systems%2C%20Richland%2C%20SC%20%282014%29) 
    
11.  Lehman, J., Stanley, K.O.: Exploiting open-endedness to solve problems through the search for novelty. In: Proceedings of the Eleventh International Conference on Artificial Life. MIT Press (2004)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Lehman%2C%20J.%2C%20Stanley%2C%20K.O.%3A%20Exploiting%20open-endedness%20to%20solve%20problems%20through%20the%20search%20for%20novelty.%20In%3A%20Proceedings%20of%20the%20Eleventh%20International%20Conference%20on%20Artificial%20Life.%20MIT%20Press%20%282004%29) 
    
12.  de Lima, E.S., Feijó, B., Furtado, A.L.: Procedural generation of quests for games using genetic algorithms and automated planning. In: 18th Brazilian Symposium on Computer Games and Digital Entertainment, SBGames 2019, Rio de Janeiro, Brazil, 28–31 October 2019, pp. 144–153. IEEE (2019). [https://doi.org/10.1109/SBGames.2019.00028](https://doi.org/10.1109/SBGames.2019.00028)
    
13.  McIntyre, N., Lapata, M.: Plot induction and evolutionary search for story generation. In: Proceedings of the 48th Annual Meeting of the Association for Computational Linguistics, pp. 1562–1572. Association for Computational Linguistics, Uppsala, Sweden, July 2010. [https://aclanthology.org/P10-1158](https://aclanthology.org/P10-1158)
    
14.  Peinado, F., Francisco, V., Hervás, R., Gervás, P.: Assessing the novelty of computer-generated narratives using empirical metrics. Minds Mach. **20**(4), 588 (2010). [https://doi.org/10.1007/s11023-010-9209-8](https://doi.org/10.1007/s11023-010-9209-8)
    
    [CrossRef](https://doi.org/10.1007%2Fs11023-010-9209-8)  [Google Scholar](https://scholar.google.com/scholar_lookup?&title=Assessing%20the%20novelty%20of%20computer-generated%20narratives%20using%20empirical%20metrics&journal=Minds%20Mach.&doi=10.1007%2Fs11023-010-9209-8&volume=20&issue=4&publication_year=2010&author=Peinado%2CF&author=Francisco%2CV&author=Herv%C3%A1s%2CR&author=Gerv%C3%A1s%2CP) 
    
15.  Pérez y Pérez, R., Sharples, M.: Mexica: a computer model of a cognitive account of creative writing. J. Exp. Theor. Artif. Intell. **13**(2), 119–139 (2001)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=P%C3%A9rez%20y%20P%C3%A9rez%2C%20R.%2C%20Sharples%2C%20M.%3A%20Mexica%3A%20a%20computer%20model%20of%20a%20cognitive%20account%20of%20creative%20writing.%20J.%20Exp.%20Theor.%20Artif.%20Intell.%2013%282%29%2C%20119%E2%80%93139%20%282001%29) 
    
16.  Porteous, J., Charles, F., Cavazza, M.: Plan-based narrative generation with coordinated subplots. In: European Conference on Artificial Intelligence (ECAI 2016), vol. 285, pp. 846–854. IOS Press (2016)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Porteous%2C%20J.%2C%20Charles%2C%20F.%2C%20Cavazza%2C%20M.%3A%20Plan-based%20narrative%20generation%20with%20coordinated%20subplots.%20In%3A%20European%20Conference%20on%20Artificial%20Intelligence%20%28ECAI%202016%29%2C%20vol.%20285%2C%20pp.%20846%E2%80%93854.%20IOS%20Press%20%282016%29) 
    
17.  Reiter, E., Dale, R.: Building Natural Language Generation Systems. Cambridge University Press, Cambridge (2000)
    
    [CrossRef](https://doi.org/10.1017%2FCBO9780511519857)  [Google Scholar](https://scholar.google.com/scholar_lookup?&title=Building%20Natural%20Language%20Generation%20Systems&publication_year=2000&author=Reiter%2CE&author=Dale%2CR) 
    
18.  Gómez de Silva Garza, A.: An evolutionary approach to design case adaptation. Ph.D. thesis, The University of Sydney, Australia (2000)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=G%C3%B3mez%20de%20Silva%20Garza%2C%20A.%3A%20An%20evolutionary%20approach%20to%20design%20case%20adaptation.%20Ph.D.%20thesis%2C%20The%20University%20of%20Sydney%2C%20Australia%20%282000%29) 
    
19.  de Silva Garza, A.G., y Pérez, R.P.: Towards evolutionary story generation. In: Colton, S., Ventura, D., Lavrac, N., Cook, M. (eds.) Proceedings of the Fifth International Conference on Computational Creativity, ICCC 2014, Ljubljana, Slovenia, 10–13 June 2014, pp. 332–335. computationalcreativity.net (2014). [http://computationalcreativity.net/iccc2014/wp-content/uploads/2014/06/15.3\_Garza.pdf](http://computationalcreativity.net/iccc2014/wp-content/uploads/2014/06/15.3_Garza.pdf)
    
20.  Tapscott, A., Gomez, J., León, C., Smailovic, J., Znidarsic, M., Gervás, P.: Empirical evidence of the limits of automatic assessment of fictional ideation. In: C3GI ESSLLI (2016)
    
    [Google Scholar](https://scholar.google.com/scholar?&q=Tapscott%2C%20A.%2C%20Gomez%2C%20J.%2C%20Le%C3%B3n%2C%20C.%2C%20Smailovic%2C%20J.%2C%20Znidarsic%2C%20M.%2C%20Gerv%C3%A1s%2C%20P.%3A%20Empirical%20evidence%20of%20the%20limits%20of%20automatic%20assessment%20of%20fictional%20ideation.%20In%3A%20C3GI%20ESSLLI%20%282016%29) 
    

[Download references](https://citation-needed.springer.com/v2/references/10.1007/978-3-031-03789-4_5?format=refman&flavour=references)

## Author information

### Authors and Affiliations

1.  Facultad de Informática, Universidad Complutense de Madrid, 28040, Madrid, Spain
    
    Pablo Gervás, Eugenio Concepción & Gonzalo Méndez
    

Authors

1.  Pablo Gervás
    
    You can also search for this author in [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=search&term=Pablo%20Gerv%C3%A1s) [Google Scholar](http://scholar.google.co.uk/scholar?as_q=&num=10&btnG=Search+Scholar&as_epq=&as_oq=&as_eq=&as_occt=any&as_sauthors=%22Pablo%20Gerv%C3%A1s%22&as_publication=&as_ylo=&as_yhi=&as_allsubj=all&hl=en)
    
2.  Eugenio Concepción
    
    You can also search for this author in [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=search&term=Eugenio%20Concepci%C3%B3n) [Google Scholar](http://scholar.google.co.uk/scholar?as_q=&num=10&btnG=Search+Scholar&as_epq=&as_oq=&as_eq=&as_occt=any&as_sauthors=%22Eugenio%20Concepci%C3%B3n%22&as_publication=&as_ylo=&as_yhi=&as_allsubj=all&hl=en)
    
3.  Gonzalo Méndez
    
    You can also search for this author in [PubMed](http://www.ncbi.nlm.nih.gov/entrez/query.fcgi?cmd=search&term=Gonzalo%20M%C3%A9ndez) [Google Scholar](http://scholar.google.co.uk/scholar?as_q=&num=10&btnG=Search+Scholar&as_epq=&as_oq=&as_eq=&as_occt=any&as_sauthors=%22Gonzalo%20M%C3%A9ndez%22&as_publication=&as_ylo=&as_yhi=&as_allsubj=all&hl=en)
    

### Corresponding author

Correspondence to [Pablo Gervás](mailto:pgervas@ucm.es) .

## Editor information

### Editors and Affiliations

1.  University of Coimbra, Coimbra, Portugal
    
    Tiago Martins
    
2.  University of A Coruña, A Coruña, Spain
    
    Nereida Rodríguez-Fernández
    
3.  University of Coimbra, Coimbra, Portugal
    
    Sérgio M. Rebelo
    

## Rights and permissions

## Copyright information

© 2022 The Author(s), under exclusive license to Springer Nature Switzerland AG

## About this paper

[![Verify currency and authenticity via CrossMark](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjgxIiB3aWR0aD0iNTciIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGcgZmlsbD0ibm9uZSIgZmlsbC1ydWxlPSJldmVub2RkIj48cGF0aCBkPSJtMTcuMzUgMzUuNDUgMjEuMy0xNC4ydi0xNy4wM2gtMjEuMyIgZmlsbD0iIzk4OTg5OCIvPjxwYXRoIGQ9Im0zOC42NSAzNS40NS0yMS4zLTE0LjJ2LTE3LjAzaDIxLjMiIGZpbGw9IiM3NDc0NzQiLz48cGF0aCBkPSJtMjggLjVjLTEyLjk4IDAtMjMuNSAxMC41Mi0yMy41IDIzLjVzMTAuNTIgMjMuNSAyMy41IDIzLjUgMjMuNS0xMC41MiAyMy41LTIzLjVjMC02LjIzLTIuNDgtMTIuMjEtNi44OC0xNi42Mi00LjQxLTQuNC0xMC4zOS02Ljg4LTE2LjYyLTYuODh6bTAgNDEuMjVjLTkuOCAwLTE3Ljc1LTcuOTUtMTcuNzUtMTcuNzVzNy45NS0xNy43NSAxNy43NS0xNy43NSAxNy43NSA3Ljk1IDE3Ljc1IDE3Ljc1YzAgNC43MS0xLjg3IDkuMjItNS4yIDEyLjU1cy03Ljg0IDUuMi0xMi41NSA1LjJ6IiBmaWxsPSIjNTM1MzUzIi8+PHBhdGggZD0ibTQxIDM2Yy01LjgxIDYuMjMtMTUuMjMgNy40NS0yMi40MyAyLjktNy4yMS00LjU1LTEwLjE2LTEzLjU3LTcuMDMtMjEuNWwtNC45Mi0zLjExYy00Ljk1IDEwLjctMS4xOSAyMy40MiA4Ljc4IDI5LjcxIDkuOTcgNi4zIDIzLjA3IDQuMjIgMzAuNi00Ljg2eiIgZmlsbD0iIzljOWM5YyIvPjxwYXRoIGQ9Im0uMiA1OC40NWMwLS43NS4xMS0xLjQyLjMzLTIuMDFzLjUyLTEuMDkuOTEtMS41Yy4zOC0uNDEuODMtLjczIDEuMzQtLjk0LjUxLS4yMiAxLjA2LS4zMiAxLjY1LS4zMi41NiAwIDEuMDYuMTEgMS41MS4zNS40NC4yMy44MS41IDEuMS44MWwtLjkxIDEuMDFjLS4yNC0uMjQtLjQ5LS40Mi0uNzUtLjU2LS4yNy0uMTMtLjU4LS4yLS45My0uMi0uMzkgMC0uNzMuMDgtMS4wNS4yMy0uMzEuMTYtLjU4LjM3LS44MS42Ni0uMjMuMjgtLjQxLjYzLS41MyAxLjA0LS4xMy40MS0uMTkuODgtLjE5IDEuMzkgMCAxLjA0LjIzIDEuODYuNjggMi40Ni40NS41OSAxLjA2Ljg4IDEuODQuODguNDEgMCAuNzctLjA3IDEuMDctLjIzcy41OS0uMzkuODUtLjY4bC45MSAxYy0uMzguNDMtLjguNzYtMS4yOC45OS0uNDcuMjItMSAuMzQtMS41OC4zNC0uNTkgMC0xLjEzLS4xLTEuNjQtLjMxLS41LS4yLS45NC0uNTEtMS4zMS0uOTEtLjM4LS40LS42Ny0uOS0uODgtMS40OC0uMjItLjU5LS4zMy0xLjI2LS4zMy0yLjAyem04LjQtNS4zM2gxLjYxdjIuNTRsLS4wNSAxLjMzYy4yOS0uMjcuNjEtLjUxLjk2LS43MnMuNzYtLjMxIDEuMjQtLjMxYy43MyAwIDEuMjcuMjMgMS42MS43MS4zMy40Ny41IDEuMTQuNSAyLjAydjQuMzFoLTEuNjF2LTQuMWMwLS41Ny0uMDgtLjk3LS4yNS0xLjIxLS4xNy0uMjMtLjQ1LS4zNS0uODMtLjM1LS4zIDAtLjU2LjA4LS43OS4yMi0uMjMuMTUtLjQ5LjM2LS43OC42NHY0LjhoLTEuNjF6bTcuMzcgNi40NWMwLS41Ni4wOS0xLjA2LjI2LTEuNTEuMTgtLjQ1LjQyLS44My43MS0xLjE0LjI5LS4zLjYzLS41NCAxLjAxLS43MS4zOS0uMTcuNzgtLjI1IDEuMTgtLjI1LjQ3IDAgLjg4LjA4IDEuMjMuMjQuMzYuMTYuNjUuMzguODkuNjdzLjQyLjYzLjU0IDEuMDNjLjEyLjQxLjE4Ljg0LjE4IDEuMzIgMCAuMzItLjAyLjU3LS4wNy43NmgtNC4zNmMuMDcuNjIuMjkgMS4xLjY1IDEuNDQuMzYuMzMuODIuNSAxLjM4LjUuMjkgMCAuNTctLjA0LjgzLS4xM3MuNTEtLjIxLjc2LS4zN2wuNTUgMS4wMWMtLjMzLjIxLS42OS4zOS0xLjA5LjUzLS40MS4xNC0uODMuMjEtMS4yNi4yMS0uNDggMC0uOTItLjA4LTEuMzQtLjI1LS40MS0uMTYtLjc2LS40LTEuMDctLjctLjMxLS4zMS0uNTUtLjY5LS43Mi0xLjEzLS4xOC0uNDQtLjI2LS45NS0uMjYtMS41MnptNC42LS42MmMwLS41NS0uMTEtLjk4LS4zNC0xLjI4LS4yMy0uMzEtLjU4LS40Ny0xLjA2LS40Ny0uNDEgMC0uNzcuMTUtMS4wNy40NS0uMzEuMjktLjUuNzMtLjU4IDEuM3ptMi41LjYyYzAtLjU3LjA5LTEuMDguMjgtMS41My4xOC0uNDQuNDMtLjgyLjc1LTEuMTNzLjY5LS41NCAxLjEtLjcxYy40Mi0uMTYuODUtLjI0IDEuMzEtLjI0LjQ1IDAgLjg0LjA4IDEuMTcuMjNzLjYxLjM0Ljg1LjU3bC0uNzcgMS4wMmMtLjE5LS4xNi0uMzgtLjI4LS41Ni0uMzctLjE5LS4wOS0uMzktLjE0LS42MS0uMTQtLjU2IDAtMS4wMS4yMS0xLjM1LjYzLS4zNS40MS0uNTIuOTctLjUyIDEuNjcgMCAuNjkuMTcgMS4yNC41MSAxLjY2LjM0LjQxLjc4LjYyIDEuMzIuNjIuMjggMCAuNTQtLjA2Ljc4LS4xNy4yNC0uMTIuNDUtLjI2LjY0LS40MmwuNjcgMS4wM2MtLjMzLjI5LS42OS41MS0xLjA4LjY1LS4zOS4xNS0uNzguMjMtMS4xOC4yMy0uNDYgMC0uOS0uMDgtMS4zMS0uMjQtLjQtLjE2LS43NS0uMzktMS4wNS0uN3MtLjUzLS42OS0uNy0xLjEzYy0uMTctLjQ1LS4yNS0uOTYtLjI1LTEuNTN6bTYuOTEtNi40NWgxLjU4djYuMTdoLjA1bDIuNTQtMy4xNmgxLjc3bC0yLjM1IDIuOCAyLjU5IDQuMDdoLTEuNzVsLTEuNzctMi45OC0xLjA4IDEuMjN2MS43NWgtMS41OHptMTMuNjkgMS4yN2MtLjI1LS4xMS0uNS0uMTctLjc1LS4xNy0uNTggMC0uODcuMzktLjg3IDEuMTZ2Ljc1aDEuMzR2MS4yN2gtMS4zNHY1LjZoLTEuNjF2LTUuNmgtLjkydi0xLjJsLjkyLS4wN3YtLjcyYzAtLjM1LjA0LS42OC4xMy0uOTguMDgtLjMxLjIxLS41Ny40LS43OXMuNDItLjM5LjcxLS41MWMuMjgtLjEyLjYzLS4xOCAxLjA0LS4xOC4yNCAwIC40OC4wMi42OS4wNy4yMi4wNS40MS4xLjU3LjE3em0uNDggNS4xOGMwLS41Ny4wOS0xLjA4LjI3LTEuNTMuMTctLjQ0LjQxLS44Mi43Mi0xLjEzLjMtLjMxLjY1LS41NCAxLjA0LS43MS4zOS0uMTYuOC0uMjQgMS4yMy0uMjRzLjg0LjA4IDEuMjQuMjRjLjQuMTcuNzQuNCAxLjA0Ljcxcy41NC42OS43MiAxLjEzYy4xOS40NS4yOC45Ni4yOCAxLjUzcy0uMDkgMS4wOC0uMjggMS41M2MtLjE4LjQ0LS40Mi44Mi0uNzIgMS4xM3MtLjY0LjU0LTEuMDQuNy0uODEuMjQtMS4yNC4yNC0uODQtLjA4LTEuMjMtLjI0LS43NC0uMzktMS4wNC0uN2MtLjMxLS4zMS0uNTUtLjY5LS43Mi0xLjEzLS4xOC0uNDUtLjI3LS45Ni0uMjctMS41M3ptMS42NSAwYzAgLjY5LjE0IDEuMjQuNDMgMS42Ni4yOC40MS42OC42MiAxLjE4LjYyLjUxIDAgLjktLjIxIDEuMTktLjYyLjI5LS40Mi40NC0uOTcuNDQtMS42NiAwLS43LS4xNS0xLjI2LS40NC0xLjY3LS4yOS0uNDItLjY4LS42My0xLjE5LS42My0uNSAwLS45LjIxLTEuMTguNjMtLjI5LjQxLS40My45Ny0uNDMgMS42N3ptNi40OC0zLjQ0aDEuMzNsLjEyIDEuMjFoLjA1Yy4yNC0uNDQuNTQtLjc5Ljg4LTEuMDIuMzUtLjI0LjctLjM2IDEuMDctLjM2LjMyIDAgLjU5LjA1Ljc4LjE0bC0uMjggMS40LS4zMy0uMDljLS4xMS0uMDEtLjIzLS4wMi0uMzgtLjAyLS4yNyAwLS41Ni4xLS44Ni4zMXMtLjU1LjU4LS43NyAxLjF2NC4yaC0xLjYxem0tNDcuODcgMTVoMS42MXY0LjFjMCAuNTcuMDguOTcuMjUgMS4yLjE3LjI0LjQ0LjM1LjgxLjM1LjMgMCAuNTctLjA3LjgtLjIyLjIyLS4xNS40Ny0uMzkuNzMtLjczdi00LjdoMS42MXY2Ljg3aC0xLjMybC0uMTItMS4wMWgtLjA0Yy0uMy4zNi0uNjMuNjQtLjk4Ljg2LS4zNS4yMS0uNzYuMzItMS4yNC4zMi0uNzMgMC0xLjI3LS4yNC0xLjYxLS43MS0uMzMtLjQ3LS41LTEuMTQtLjUtMi4wMnptOS40NiA3LjQzdjIuMTZoLTEuNjF2LTkuNTloMS4zM2wuMTIuNzJoLjA1Yy4yOS0uMjQuNjEtLjQ1Ljk3LS42My4zNS0uMTcuNzItLjI2IDEuMS0uMjYuNDMgMCAuODEuMDggMS4xNS4yNC4zMy4xNy42MS40Ljg0LjcxLjI0LjMxLjQxLjY4LjUzIDEuMTEuMTMuNDIuMTkuOTEuMTkgMS40NCAwIC41OS0uMDkgMS4xMS0uMjUgMS41Ny0uMTYuNDctLjM4Ljg1LS42NSAxLjE2LS4yNy4zMi0uNTguNTYtLjk0LjczLS4zNS4xNi0uNzIuMjUtMS4xLjI1LS4zIDAtLjYtLjA3LS45LS4ycy0uNTktLjMxLS44Ny0uNTZ6bTAtMi4zYy4yNi4yMi41LjM3LjczLjQ1LjI0LjA5LjQ2LjEzLjY2LjEzLjQ2IDAgLjg0LS4yIDEuMTUtLjYuMzEtLjM5LjQ2LS45OC40Ni0xLjc3IDAtLjY5LS4xMi0xLjIyLS4zNS0xLjYxLS4yMy0uMzgtLjYxLS41Ny0xLjEzLS41Ny0uNDkgMC0uOTkuMjYtMS41Mi43N3ptNS44Ny0xLjY5YzAtLjU2LjA4LTEuMDYuMjUtMS41MS4xNi0uNDUuMzctLjgzLjY1LTEuMTQuMjctLjMuNTgtLjU0LjkzLS43MXMuNzEtLjI1IDEuMDgtLjI1Yy4zOSAwIC43My4wNyAxIC4yLjI3LjE0LjU0LjMyLjgxLjU1bC0uMDYtMS4xdi0yLjQ5aDEuNjF2OS44OGgtMS4zM2wtLjExLS43NGgtLjA2Yy0uMjUuMjUtLjU0LjQ2LS44OC42NC0uMzMuMTgtLjY5LjI3LTEuMDYuMjctLjg3IDAtMS41Ni0uMzItMi4wNy0uOTVzLS43Ni0xLjUxLS43Ni0yLjY1em0xLjY3LS4wMWMwIC43NC4xMyAxLjMxLjQgMS43LjI2LjM4LjY1LjU4IDEuMTUuNTguNTEgMCAuOTktLjI2IDEuNDQtLjc3di0zLjIxYy0uMjQtLjIxLS40OC0uMzYtLjctLjQ1LS4yMy0uMDgtLjQ2LS4xMi0uNy0uMTItLjQ1IDAtLjgyLjE5LTEuMTMuNTktLjMxLjM5LS40Ni45NS0uNDYgMS42OHptNi4zNSAxLjU5YzAtLjczLjMyLTEuMy45Ny0xLjcxLjY0LS40IDEuNjctLjY4IDMuMDgtLjg0IDAtLjE3LS4wMi0uMzQtLjA3LS41MS0uMDUtLjE2LS4xMi0uMy0uMjItLjQzcy0uMjItLjIyLS4zOC0uM2MtLjE1LS4wNi0uMzQtLjEtLjU4LS4xLS4zNCAwLS42OC4wNy0xIC4ycy0uNjMuMjktLjkzLjQ3bC0uNTktMS4wOGMuMzktLjI0LjgxLS40NSAxLjI4LS42My40Ny0uMTcuOTktLjI2IDEuNTQtLjI2Ljg2IDAgMS41MS4yNSAxLjkzLjc2cy42MyAxLjI1LjYzIDIuMjF2NC4wN2gtMS4zMmwtLjEyLS43NmgtLjA1Yy0uMy4yNy0uNjMuNDgtLjk4LjY2cy0uNzMuMjctMS4xNC4yN2MtLjYxIDAtMS4xLS4xOS0xLjQ4LS41Ni0uMzgtLjM2LS41Ny0uODUtLjU3LTEuNDZ6bTEuNTctLjEyYzAgLjMuMDkuNTMuMjcuNjcuMTkuMTQuNDIuMjEuNzEuMjEuMjggMCAuNTQtLjA3Ljc3LS4ycy40OC0uMzEuNzMtLjU2di0xLjU0Yy0uNDcuMDYtLjg2LjEzLTEuMTguMjMtLjMxLjA5LS41Ny4xOS0uNzYuMzFzLS4zMy4yNS0uNDEuNGMtLjA5LjE1LS4xMy4zMS0uMTMuNDh6bTYuMjktMy42M2gtLjk4di0xLjJsMS4wNi0uMDcuMi0xLjg4aDEuMzR2MS44OGgxLjc1djEuMjdoLTEuNzV2My4yOGMwIC44LjMyIDEuMi45NyAxLjIuMTIgMCAuMjQtLjAxLjM3LS4wNC4xMi0uMDMuMjQtLjA3LjM0LS4xMWwuMjggMS4xOWMtLjE5LjA2LS40LjEyLS42NC4xNy0uMjMuMDUtLjQ5LjA4LS43Ni4wOC0uNCAwLS43NC0uMDYtMS4wMi0uMTgtLjI3LS4xMy0uNDktLjMtLjY3LS41Mi0uMTctLjIxLS4zLS40OC0uMzctLjc4LS4wOC0uMy0uMTItLjY0LS4xMi0xLjAxem00LjM2IDIuMTdjMC0uNTYuMDktMS4wNi4yNy0xLjUxcy40MS0uODMuNzEtMS4xNGMuMjktLjMuNjMtLjU0IDEuMDEtLjcxLjM5LS4xNy43OC0uMjUgMS4xOC0uMjUuNDcgMCAuODguMDggMS4yMy4yNC4zNi4xNi42NS4zOC44OS42N3MuNDIuNjMuNTQgMS4wM2MuMTIuNDEuMTguODQuMTggMS4zMiAwIC4zMi0uMDIuNTctLjA3Ljc2aC00LjM3Yy4wOC42Mi4yOSAxLjEuNjUgMS40NC4zNi4zMy44Mi41IDEuMzguNS4zIDAgLjU4LS4wNC44NC0uMTMuMjUtLjA5LjUxLS4yMS43Ni0uMzdsLjU0IDEuMDFjLS4zMi4yMS0uNjkuMzktMS4wOS41M3MtLjgyLjIxLTEuMjYuMjFjLS40NyAwLS45Mi0uMDgtMS4zMy0uMjUtLjQxLS4xNi0uNzctLjQtMS4wOC0uNy0uMy0uMzEtLjU0LS42OS0uNzItMS4xMy0uMTctLjQ0LS4yNi0uOTUtLjI2LTEuNTJ6bTQuNjEtLjYyYzAtLjU1LS4xMS0uOTgtLjM0LTEuMjgtLjIzLS4zMS0uNTgtLjQ3LTEuMDYtLjQ3LS40MSAwLS43Ny4xNS0xLjA4LjQ1LS4zMS4yOS0uNS43My0uNTcgMS4zem0zLjAxIDIuMjNjLjMxLjI0LjYxLjQzLjkyLjU3LjMuMTMuNjMuMi45OC4yLjM4IDAgLjY1LS4wOC44My0uMjNzLjI3LS4zNS4yNy0uNmMwLS4xNC0uMDUtLjI2LS4xMy0uMzctLjA4LS4xLS4yLS4yLS4zNC0uMjgtLjE0LS4wOS0uMjktLjE2LS40Ny0uMjNsLS41My0uMjJjLS4yMy0uMDktLjQ2LS4xOC0uNjktLjMtLjIzLS4xMS0uNDQtLjI0LS42Mi0uNHMtLjMzLS4zNS0uNDUtLjU1Yy0uMTItLjIxLS4xOC0uNDYtLjE4LS43NSAwLS42MS4yMy0xLjEuNjgtMS40OS40NC0uMzggMS4wNi0uNTcgMS44My0uNTcuNDggMCAuOTEuMDggMS4yOS4yNXMuNzEuMzYuOTkuNTdsLS43NC45OGMtLjI0LS4xNy0uNDktLjMyLS43My0uNDItLjI1LS4xMS0uNTEtLjE2LS43OC0uMTYtLjM1IDAtLjYuMDctLjc2LjIxLS4xNy4xNS0uMjUuMzMtLjI1LjU0IDAgLjE0LjA0LjI2LjEyLjM2cy4xOC4xOC4zMS4yNmMuMTQuMDcuMjkuMTQuNDYuMjFsLjU0LjE5Yy4yMy4wOS40Ny4xOC43LjI5cy40NC4yNC42NC40Yy4xOS4xNi4zNC4zNS40Ni41OC4xMS4yMy4xNy41LjE3LjgyIDAgLjMtLjA2LjU4LS4xNy44My0uMTIuMjYtLjI5LjQ4LS41MS42OC0uMjMuMTktLjUxLjM0LS44NC40NS0uMzQuMTEtLjcyLjE3LTEuMTUuMTctLjQ4IDAtLjk1LS4wOS0xLjQxLS4yNy0uNDYtLjE5LS44Ni0uNDEtMS4yLS42OHoiIGZpbGw9IiM1MzUzNTMiLz48L2c+PC9zdmc+)](https://crossmark.crossref.org/dialog/?doi=10.1007/978-3-031-03789-4_5)

### Cite this paper

Gervás, P., Concepción, E., Méndez, G. (2022). Evolutionary Construction of Stories that Combine Several Plot Lines. In: Martins, T., Rodríguez-Fernández, N., Rebelo, S.M. (eds) Artificial Intelligence in Music, Sound, Art and Design. EvoMUSART 2022. Lecture Notes in Computer Science, vol 13221. Springer, Cham. https://doi.org/10.1007/978-3-031-03789-4\_5

### Download citation

-   [.RIS](https://citation-needed.springer.com/v2/references/10.1007/978-3-031-03789-4_5?format=refman&flavour=citation "Download this article's citation as a .RIS file")
-   [.ENW](https://citation-needed.springer.com/v2/references/10.1007/978-3-031-03789-4_5?format=endnote&flavour=citation "Download this article's citation as a .ENW file")
-   [.BIB](https://citation-needed.springer.com/v2/references/10.1007/978-3-031-03789-4_5?format=bibtex&flavour=citation "Download this article's citation as a .BIB file")

-   DOI: https://doi.org/10.1007/978-3-031-03789-4\_5
    
-   Published: 15 April 2022
    
-   Publisher Name: Springer, Cham
    
-   Print ISBN: 978-3-031-03788-7
    
-   Online ISBN: 978-3-031-03789-4
    
-   eBook Packages: [Computer Science](https://link.springer.com/search?facet-content-type=%22Book%22&package=11645&facet-start-year=2022&facet-end-year=2022)[Computer Science (R0)](https://link.springer.com/search?facet-content-type=%22Book%22&package=43710&facet-start-year=2022&facet-end-year=2022)
