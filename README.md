# Tasksumltion
permutations and combinations
by Alli gamal Aziz

from itertools import chain, combinations

def powerset(iterable):
    s = list(iterable)  # allows duplicate elements
    return chain.from_iterable(combinations(s, r) for r in range(len(s)+1))
number= int(input("How many number do you want? (MAX 26): "))
A_LIST=[]
p = []
for i in range(number):
    for index in range(0, len(A_LIST)):
        print(index, A_LIST[index])
    a = int(input("Select a number: "))
    p.append(a)
#stuff = [1, 2, 3]
for i, combo in enumerate(powerset(p), 1):
    print('combo #{}: {}'.format(i, combo))
