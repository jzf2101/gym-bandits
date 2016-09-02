# Bandit Envs

Series of Bandit Envs for the OpenAI Gym

Each env uses a different set of:

Probability Distributions - A list of probabilities of the likelihood that a particular bandit will pay out

Reward Distributions - A list of either rewards (if number) or means and standard deviations (if list) of the payout that bandit has

E.g. BanditTwoArmedHighLowFixed-v0 has p_dist=[0.8, 0.2], r_dist=[1, 1], meaning 80% of the time that action 0 is
selected it will payout 1, and 20% of the time action 2 is selected it will payout 1

Fixed means these distributions are set
Random means the distributions are generated on the fly when the env is first loaded

You can access the distributions through the p_dist and r_dist variables if you want to match
your weights against the true values for plotting results of various algorithms

Contains:
* BanditTenArmedRandomFixed-v0: 10 armed bandit with random probabilities assigned to payouts
* BanditTenArmedRandomRandom-v0: 10 armed bandit with random probabilities assigned to both payouts and rewards
* BanditTenArmedRandomStochastic-v0: 10 armed bandit with random probabilities assigned to payouts, and reward are selected from a distribution
* BanditTwoArmedDeterministicFixed-v0: Simplest case where one bandit always pays, and the other always doesn't
* BanditTwoArmedHighHighFixed-v0: Stochastic version with a small difference between which bandit pays where both are good
* BanditTwoArmedHighLowFixed-v0: Stochastic version with a large difference between which bandit pays out of two choices
* BanditTwoArmedHighLowFixedNegative-v0: Stochastic version where one bandit pays out negative with a large percent
* BanditTwoArmedLowLowFixed-v0: Stochastic version with a small difference between which bandit pays where both are bad