# Risky Lottery

https://open.kattis.com/problems/riskylottery

Risky Lottery is a deceptively simple probability problem. It requires a few insights. The first is that the error bounds allow an iterative method to finding a solution to work fast enough. The next is that in an optimal solution, the probability of winning with each possible number chosen is proportional to how often we want to choose it. Say instead that we have the opposite: Choosing 0 is 2x more likely to result in a win than choosing 1 - we could now create a better strategy by choosing 0 more often and capitalizing on the increased chances of winning. The final insight is that we can calculate the probability of winning with each number by taking them in order, calculating the different moves we could make and probability of remaining counts, and storing the possibility of winning at each stage as we go. I've tested several other methods for doing this calculation and found no others that are nearly this simple.