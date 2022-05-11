# Continuous Blackjack

In this notebook, the continuous blackjack game, which was introduced in *G-Research Virtual Quant Finance Algorithmic Challenge (Japan, Online)* will be discussed. This is a partial summary of  [Mu Zhao's note](https://arxiv.org/abs/2011.10315) who completed the math Ph.D. in Stony Brook University with me and attended this challenge together as a team. I wrote this note for myself to achieve the concrete understanding on this problem with the practice on programming.

The problem is described as follows. Let $\{P_1,\cdots,P_n\}$ be players in the game. Then we will repeat the following game for $N$ times.
1. First, we choose each player's turn using a bijection $\sigma : \{1,\cdots,n\} \to \{1,\cdots,n\}$. Then the game proceeds with the order of $(P_{\sigma(1)},\cdots,P_{\sigma(n)})$.
2. In each player's turn, the player will receive the random number that is uniformly distributed in $[0,1]$. You can receive cards as many as you want, but if you bust (i.e. if the sum of your hands is bigger than 1), then you will automatically lose the game. Your goal is to be a player with the maximum hand that is not busted after all players finished their turn.
3. In your turn, you can see all of your previous players' hands. 
4. For each game, the winner will receive a point. 
5. After $N$ games are finished, we compute the total score and determine the final winner of this game.

More details are included in a notebook file.