# Bayesian-Statistics-Activity-3
Activity 3: Coding the sample attachments in Python

Script/Code (1st Picture)

calculate the probability of cancer patient and diagnostic test

calculate P(A|B) given P(A), P(B|A), P(B|not A)

def bayes_theorem(p_a, p_b_given_a, p_b_given_not_a):
    # calculate P(not A)
    not_a = 1 - p_a
    # calculate P(B)
    p_b = p_b_given_a * p_a + p_b_given_not_a * not_a
    # calculate P(A|B)
    p_a_given_b = (p_b_given_a * p_a) / p_b
    return p_a_given_b

#P(A)
p_a = 0.0002
#P(B|A)
p_b_given_a = 0.85
#P(B|not A)
p_b_given_not_a = 0.05
#calculate P(A|B)
result = bayes_theorem(p_a, p_b_given_a, p_b_given_not_a)
#summarize
print('P(A|B) = %.3f%%' % (result * 100))


Script/Code (2nd Picture)

import numpy as np
import matplotlib.pyplot as plt

prior_probs = np.array([[0.33,0.3], [0.2,0.17]])

plt.imshow(prior_probs, cmap='gray')
plt.colorbar()

for i in range(2):
    for j in range(2):
        plt.annotate(prior_probs[i,j], (j,i), color="red", fontsize=20, fontweight='bold', ha='center', va='center')
        
plt.title('Prior Probabilities', fontsize=20)   


Screenshot of the Output

![activity 3 1](https://github.com/mariachrislenereis/Bayesian-Statistics-Activity-3/assets/168893458/0c994ccd-7d43-4eb0-bcae-567c6bde2c23)


![activity 3 2](https://github.com/mariachrislenereis/Bayesian-Statistics-Activity-3/assets/168893458/a0bb4a6a-2308-4eb9-826f-cd80ecc83c3f)
