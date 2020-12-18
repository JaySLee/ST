# Symbolic trajectories {#sec:ST}

$\newcommand{\T}[1]{\text{#1}}$
$\newcommand{\tm}{\text{-}}$


## Preliminary model 

_**So, I went down a rabbit hole in trying to parse the different components/manifestations of symbolic trajectories. My inclination is to make this complicated before they can be simplified.**_

This first section appears useful (at least to me). The next sections expands on this section, but doesn't quite go anywhere yet (i.e. isn't as useful to me for the moment except as a fun exercise). Also, the formalization is not 100% consistent/airtight, yet.

First, we start with some notation.

<u>Primary definitions:</u>

- $M$ = the actual state of Moerwijk $\in \{-1,+1\}$ : "It's bad or good."
    - 'M' (un-italicized) simply refers to 'Moerwijk'
    - For simplicity, I pose only two valence states (bad v. good) for M and other things.
- $C$ = valence of user $u$'s post $\in \{-1,+1\}$; the $u$ subscript is implicit here (i.e. $C$ means $C_u$)
- $t\!-\!\!1,t,t\!+\!\!1$ = past, present, future
  - For the table below, I don't yet deal with the future, which will later be typically treated as an expected outcome (expectation).

So now, here's an enumeration of all combinations of the valences of $M$ over time (i.e. trajectories) and user's post, along with an informal explanation (off the top of my head) and a 'symbolic' category to which the combination might belong
  * Caveat #1: The grammar of the 'symbolic' heading in conjunction with my descriptive category is off in a few places.
  * Caveat #2: This table doesn't cover gentrification, branding, or re-signification. That comes in the next sections.

<u>Trajectories and post valences:</u>  

| # | $M_{t-1}$ | $M_{t}$ | $C_t$ |explanation                |symbolic ...                             |
|:-:|:---------:|:-------:|:-----:|:--------------------------|:----------------------------------------|
| 1 |    -1     |   -1    |  -1   |things suck, always awful  |reinforcing defamation                   |
| 2 |    -1     |   -1    |  +1   |put up a happy face        |hopeless optimism                        |
| 3 |    -1     |   +1    |  -1   |disbeliever of happy times |pessimistic defamation/denial of upgrade |
| 4 |    -1     |   +1    |  +1   |we're good/better now      |affirming upgrade                        |
| 5 |    +1     |   -1    |  -1   |things went to sh-t        |affirming downgrade                      |
| 6 |    +1     |   -1    |  +1   |nostalgic delusion         |denial of downgrade                      |
| 7 |    +1     |   +1    |  -1   |crazy grump/hidden agenda  |unjustified defamation                   |
| 8 |    +1     |   +1    |  +1   |always awesome             |affirmation                              |

## Expectations and Perceptions

Strictly speaking, we're not dealing with the known actual state $M$ but people's perception. When we want to incorporate future states, we'll need to think of the future in terms of people's expectation. So ...

<u>Secondary definitions:</u>

- $E(x)$ = expectation; how one believes $x$ will turn out  
- $P(x)$ = perception/belief; what one thinks of $x$ or believes what $x$ is  
  - After hashing this out some, it turns out expectation is merely perception of something that will happen in the future. So $E(x_{t+1}) = P_t(x_{t+1})$.
  - For now, we'll use these interchangeably.

Also, the introduction of $P$ means the headers of the table are inaccurate. But, the assumptions below render the table more accurate and don't break what's in the 'explanation' and 'symbolic' columns, except for maybe a few cases (see below).

<u>Simplifying assumptions:</u>

- $C_t = E_u(M_{t+1})$ : User's post also reflects what the user expects Moerwijk will be in the future
- $M_t = P_u(M_t)$ : For the sake of simplifying the notation (in the table column headers), the state of Moerwijk at a point in time is actually the user's perception of Moerwijk.

<u>Caveats:</u>

- For filling in the 'explanation' and 'symbolic' columns, I haven't been super careful about not conflating perception of and actual state of M.
- E.g., combination \#6, the description of "crazy grump" applies when it's about the actual states of Moerwijk $M$ and not the perception $P(M)$. That is, the grump may not realize things have been good and are still good, so then the grump posts a negatively valenced post.
  - "Hidden agenda" applies to when someone perceives the state to be good all around then posts negatively anyways.
- Incorporating perception ($P$) all around opens the can of worms for enumerating a full, comprehensive model which would explore all combinations of both actual states of Moerwijk $M$ and perceptions of those states $P(M)$.
  - However, some of these combinations will likely be removable due to contradiction, unlikelihood, unrealism/sheer absurdity.
  - For now, I'm hesitant to open up the "space" of combinations in order to keep things manageable.
  - If I decide to explore this formalization further, I will likely have to go open up this space.

## Extensions

So we need some extensions to the model in order to encompass other concepts such as **gentrification**, **branding**, and **re-signification**.

_Bear in mind, I don't know quite what else to do with the formalization here ... yet. Ideally, what would happen is that we conjure up some mapping between data and the model here to assess the extent of SG, SB, SR, etc. But, devil's advocate says: would not qualitative coding + an AI classifier accomplish the same thing?_

<u>Extensions:</u>

- $M$ is no longer scalar (value of -1 or +1) but can be a set containing features, namely:
  - $b$ = a feature of $M$ (e.g., used in an attempt to brand or an element of gentrification)
    - I use $b$ since I initially employed the idea of this feature for formalizing branding. In typical formalations, people use $x$.
  - So, e.g., $M_t = \{+1,b\}$ means that today, M is in a good state and also has a feature $b$ (e.g., expensive housing).
- Subscript $o$ = others or the audience (of a post), e.g., $P_u(P_o(M_t))$ = "how I, the user, think others think of present day Moerwijk"
- $\Delta y =$ Change in some value $y$ from time expressed in $y$ and one time period prior.
  - E.g., $E_u(\Delta P_o(M_{t+1})) > 0$ means the user expects others' perception of M will improve from what it is at present; $t$ is implicit.
  - $\Delta M_{t} < 0$ means M got worse from the past to present; $t-1$ is implicit.
- $U(x)$ = utility, or welfare, of some people group $x$

##  Gentrification

Gentrification can be expressed through an additional definition and two conditions:
1) Let $X$ be the population of Moerwijk
   - Some subpopulation $r$ ($r \subset X$) is the set of rich people.
   - Some subpopulation $p$ ($p \subset X$) is the set of poor people.
2) $b \in M_{t+1}, b \in M_{t}, b \notin M_{t-1}$
   * In English: "Some feature $b$ was not part of Moerwijk in the past, but it is now and will continue to be."
   * Another way to write this is:
     - $M_{t}\setminus M_{t-1} = b$ : "The difference between present day Moerwijk set and past is feature $b$."
3) $M_{t} \ni \{\Delta U_{r,t} > 0, \Delta U_{p,t} < 0\}$
   * In English: "Another feature of Moerwijk ($M$) today is that - at the same time $b$ becomes part of Moerwijk - the welfare ($U$) of some subpopulation of Moewijk ($r$ or the rich) has improved while the welfare of another subpopuation ($p$ or the poor) has diminished."
   * This is ongoing/past gentrification. Expected future gentrification would use $t+1$ and employ expectation $E$
4) Written fully, this would be:
   * $G = \{M_{t} \ni \{M_t \setminus M_{t-1} = b, \Delta U_{r,t} > 0, \Delta U_{p,t} < 0\}\}$
   * $G$ (gentrification) contains the entire thing.
   * So then $G_t \ni P_{u,t}$ means gentrification is member of user's perceptions, i.e. the user believes gentrification to be happening today.

Strictly speaking, we should be distinguishing $X_t$ and $X_{t+1}$, as the composition of the future population of Moerwijk will change through gentrification.

<u>Other notes of symbolic gentrification (SG):</u>
* Conveying something that's happening that's related to G vs. the post's actually contributing to G.
<!-- But symbolic gentrification is more complicated than that. Symbolic gentrification can be: -->
* Showcasing things that are part of gentrification:
  - Rich people moving in
  - Poor people moving out
  - Indications of new expensive housing, businesses, schools (i.e. built, being built, promise of construction)
* Showcasing things that contribute to gentrification:
  - Anything that makes rich people think "hey, I'd like to move there"
  - **Gentrification can then be a consequence of branding.**

## Branding

The following conditions define branding:

<!-- #| formula &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;&nbsp;| description | -->

#|formula   |description |
-|:---------|:----------------------|
1| $M_t \setminus M_{t-1} = b$ | "$b$ is new feature of M."|
2| $P_{uo}(M_{t}) > P_{uo}(M_{t-1})$ | "My and other people's perceptions of M have improved."
3| $C_t \ni \{b,+1\}$ | User's post contains feature $b$ and the post is positively valenced. "M is a place that has $b$ or does $b$".
4| $E_u(P_o(M_{t+1})) > 0$ | User expects others' perceptions of M's future to be positive. 
5| Optional: $\Delta P_o(M_{t+1}) > 0$ | Others' perception of M actually improves.

Note: Eq. 5 treats $t+1$ not as an expectation but a real manifestation.

Re-signification is a kind of branding and I've moved its discussion to the end of this document (because I really go down the rabbit hole there).


<!-- as rich people may move in. Also, the set $X$'s composition would change, fewer $p$ poor people. -->

## Other mechanics

- $P_u(P_o(M_{t-1}))$ : "How I think what others think Moerwijk used to be like."
- $P_u(M_{t-1}) > 0, P_u(M_{t}) < 0$ : "I think M used to be good but sucks now."
- $E_u(M_{t+1}) > 0$ : "But I believe it will become good."
- $P_u(M_t) \ne M_t$ : **An inaccurate perception of Moerwijk today. Accounting for inequalities like this one can make the 1st table REALLY complicated!!**
- $E_u(P_o(M_{t+1}| C_t > 0, 
     \{P_{u}(M_{t}),P_{u}(P_{o}(M_{t})), 
     P_{u}(M_{t-1}),
	 P_{u}(P_{o}(M_{t-1}))\} < 0)) > 0$
  * "I expect others to think better of M after my positive post given that I think, and think that others think, that Moerwijk was bad in the past and still is." -> attempt at upgrading
  * For this one, my notation $\{x,y,z\} < 0$ means all of $x<0,y<0,z<0$.
<!-- $P_a(M_{t+1})>0, P_a(M_{t+1} \ni b)$ branding -->
- $\Delta M_t = M_t - M_{t-1}$ : How M actually changed from past to today.
  * Note, this is not necessarily the same as $M_t > 0, M_{t-1} < 0$ or its converse, if we widen values beyond/within $-1$ and $+1$. E.g., M could have gotten better, but still remains "bad" today.
- $E_u(\Delta M_{t+1}) = E_u(M_{t+1} - M_{t})$ : "How I - the user - expect M will change from today into the future."
- $E_u(\Delta P_u(M_t)) = P_u(M_{t+1}) - P_u(M_t)$ - How I expect my perception of M will change in the future.
  * As I wrote in way above, there seems to be some conflation of $E$ and $P$ that will need to be resolved. Maybe get rid of $E$ altogether?
  * So then $P_{u,t}(M_{t+1})$ would mean that my perception today of M's future is an expectation.
- $\Delta P_{o,t} = P_{o,t} - P_{o,t-1}$ : How others' perception today on (un-named target) has changed from what it was in the past.
- A subtle distinction:
  * $P_{u,t-1}(M_{t-1}) < 0$ : "In the past, I thought badly of M."
  * $P_{u,t}(M_{t-1}) < 0$ : "Today, I think M of the past was bad."
  
## Other notes, issues, distinctions

- Do we distinguish outsider comment/critique (no stake in M) vs. insider?
- Each carries different kinds of legitimacy/credibility.
- It occurs to me that the insider's negative critique will be seen as more credible ...  
  ... while the outsider's positive critique will be seen as more credible.
  
## Re-signification

So resignif (SR) is similar to branding (SB) but the feature $b$ is different.

Simplest expression is to say an SR $b$ is different than an SB $b$

- $b = \{x_1,...,x_n\}$ - Now $b$ itself defined as a set of (sub)features.
- So we can assign $b_b$ as a branding feature.
- And $b_r$ to be a re-signifying feature.
- $b_b \cap b_r = \emptyset$ means things used for branding M do not share any (sub)features with things used for resignifying; obviously this is not realistic, but simpler for now.
- At this point, it becomes tricky to formally distinguish subfeatures that are "cultural" vs. non-cultural.
- To do this right, I would need to expand utility $U$ to incorporate features and/or be multidimensional.
- Ultimately, both cultural (CA) and non-cultural artifacts (NCA) eventually - after many conceptual/cognitive layers - trigger survival $U$.
  - The assertion that all utilities $U$ lead to Rome ... er ... survival is my own.
- Which raises the question: is the distinction between CA and NCA about different in features? Or maybe this ultimately becomes a difference in the length (# of hops) in the pathway of the stimulus to (neural) survival. E.g.,
  - avoiding a bullet shot at you = direct link to 'survival' utility
  - starving then finding food = slightly less direct link
  - finding your neighborhood has a new great Italian place = several hops
  - getting the warm and fuzzies from seeing a cool building or a painting = more hops
  - a new school in the neighborhood = more hops than Italian place but fewer than painting?
- Simply put, one characteristic that distinguishes CAs from NCAs is that CAs have a longer utility chain/hops to survival than NCAs.
  - Maybe this is just one of the characteristics but there are other distinguishing characteristics.



<!-- ## Symbolism -->

<!-- What makes it all "symbolic"? -->

<!-- * Post actually [does|does not] change perception -->
<!--   * Perception is (in)accurate -->
  
<!-- Post is perceived to reflect some feature $b$ or dynamic like $G$. -->
