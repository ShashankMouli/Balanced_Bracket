# Balanced_Bracket
#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the isBalanced function below.
def isBalanced(s):
    
    for i in range(len(s)//2):
        if s[i] == s[len(s)-i-1]:
            continue
        else:
            return('NO')
    return('YES')
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    t = int(input())

    for t_itr in range(t):
        s = input()

        result = isBalanced(s)

        fptr.write(result + '\n')

    fptr.close()

