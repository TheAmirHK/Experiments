# Equilibria in game theory

In game theory, an equilibrium is a concept that describes a stable state in a strategic interaction where no player has an incentive to unilaterally deviate from their chosen strategy after considering the strategies of the other players.
The most common ones can be found below and for more refer to Game Theory: An Introduction by Steven Tadelis (http://students.aiu.edu/submissions/profiles/resources/onlineBook/Y5z2A2_Game_Theory_An_Introduction.pdf)

## 1. Nash Equilibrium
  - Definition: A set of strategies where no player can improve their payoff by unilaterally changing their strategy, given the strategies of the other players.
  - Example: In the Prisoner's Dilemma, the Nash Equilibrium is for both players to defect, even though mutual cooperation would yield a better outcome.
  - #### **Mathematical Model**  
  For a game with $n$ players, let:  
- $S_i$ be the set of strategies for player $i$.  
- $s_i ∈ S_i$ be a strategy for player $i$.  
- $S_{-i}$ be the strategies of all players except player $i$.  
- $u_i(s_i, s_{-i})$ be the payoff for player $i$ when they choose $s_i$ and others choose $s_{-i}$.
- A strategy profile $s_1, s_2*, ..., s_n*$ is a **Nash Equilibrium** if:
<p align="center">
$u_i(s_i^*, s_{-i}) ≥ u_i(s_i, s_{-i}),  ∀s_i ∈ S_i, ∀{i} ∈ {1, 2, ..., n}$
</p>

## 2. Pareto Optimal Equilibrium
  - Definition: A set of strategies where no player can improve their payoff without making another player worse off.
  - Example: In the Prisoner's Dilemma, mutual cooperation is Pareto optimal because neither player can improve their payoff without the other player's payoff decreasing.
  - #### **Mathematical Model**  
A strategy profile $(s_1*, s_2*, ..., s_n*)$ is **Pareto Optimal** if there does not exist another strategy profile $(s_1, s_2, ..., s_n)$ such that:  
<p align="center">
$u_i(s_1, s_2, ..., s_n) ≥ u_i(s_1*, s_2*, ..., s_n*) ∀i ∈ {1, 2, ..., n}$
<br /> and <br />
$u_j(s_1, s_2, ..., s_n) > u_j(s_1*, s_2*, ..., s_n*)$ for some $j$
</p>
  
## 3. Dominant Strategy Equilibrium
  - Definition: A set of strategies where each player's strategy is dominant (i.e., it yields the highest payoff regardless of the other players' strategies).
  - Example: In the Prisoner's Dilemma, defecting is a dominant strategy for both players, leading to a dominant strategy equilibrium.
  - #### **Mathematical Model**  
A strategy $s_i*$ is **dominant** for player $i$ if:
<p align="center">
$u_i(s_i*, s_{-i}) ≥ u_i(s_i, s_{-i}) ∀s_i ∈ S_i, ∀s_{-i} ∈ S_{-i}$
</p>

## 4. Mixed Strategy Equilibrium
  - Definition: A set of strategies where players randomize their actions according to specific probabilities, and no player can improve their expected payoff by changing their strategy.
  - Example: In the game of Rock-Paper-Scissors, the mixed strategy equilibrium is for each player to choose Rock, Paper, or Scissors with equal probability (1/3 each).
  - #### **Mathematical Model**  
Let:
- $σ_i$ be a mixed strategy for player $i$, which is a probability distribution over $S_i$.
- $σ = (σ_1, σ_2, ..., σ_n)$ be the mixed strategies of all players.
- $u_i(σ_i, σ_{-i})$ be the expected payoff for player $i$.

A **Mixed Strategy Nash Equilibrium** satisfies:
<p align="center">
$u_i(σ_i*, σ_{-i}) ≥ u_i(σ_i, σ_{-i}), ∀σ_i, ∀i ∈ {1, 2, ..., n}$
</p>


## 5. Subgame Perfect Equilibrium
  - Definition: A refinement of Nash Equilibrium that applies to dynamic games (games played over multiple stages). It requires that the strategies form a Nash Equilibrium in every subgame of the original game.
  - Example: In a sequential bargaining game, the subgame perfect equilibrium involves players making offers and counteroffers that are optimal at every stage of the game.
  - #### **Mathematical Model**  
A strategy profile $(s_1*, s_2*, ..., s_n*)$ is a **Subgame Perfect Equilibrium** if it induces a Nash Equilibrium in every subgame of the original game.


## 6. Correlated Equilibrium
  - Definition: A set of strategies where players follow recommendations from a trusted third party (correlating device), and no player can improve their expected payoff by deviating from the recommendation.
  - Example: In a traffic light game, a traffic light acts as a correlating device, telling drivers when to go and when to stop. Following the light's signals forms a correlated equilibrium.
  - #### **Mathematical Model**  
Let $π$ be a probability distribution over the set of strategy profiles $S = S_1 × S_2 × ... × S_n$, where:  
- $π(s)$ is the probability of selecting strategy profile $s$.

A probability distribution $π$ is a **Correlated Equilibrium** if:
<p align="center">
$∑{s{-i}} π(s_i, s_{-i}) * [ u_i(s_i, s_{-i}) - u_i(s_i', s_{-i}) ] ≥ 0, ∀s_i, s_i' ∈ S_i, and ∀i∈{1,2,...,n}$
</p>

## 7. Evolutionarily Stable Strategy (ESS)
  - Definition: A strategy that, if adopted by a population, cannot be invaded by any alternative strategy. It is a concept from evolutionary game theory.
  - Example: In the Hawk-Dove game, a population of doves (cooperators) can be invaded by hawks (defectors), but a mixed population of hawks and doves can form an evolutionarily stable strategy.

## 8. Bayesian Nash Equilibrium
  - Definition: A set of strategies where players maximize their expected payoffs given their beliefs about the other players' types (which may be uncertain).
  - Example: In an auction with incomplete information, bidders submit bids based on their beliefs about the other bidders' valuations, forming a Bayesian Nash Equilibrium.

## 9. Trembling Hand Perfect Equilibrium
  - Definition: A refinement of Nash Equilibrium where players' strategies are robust to small mistakes (trembles) in their actions.
  - Example: In a coordination game, a trembling hand perfect equilibrium ensures that players choose strategies that are optimal even if there is a small chance of making a mistake.

10. Coalition-Proof Equilibrium
Definition: A set of strategies where no subset of players can form a coalition and jointly deviate to improve their payoffs.

Example: In a voting game, a coalition-proof equilibrium ensures that no group of voters can collude to change the outcome in their favor.
