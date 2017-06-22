# Python-INFO1-CE9990
"""inputoutput

Program to find the present value of a bond
"""

import sys

try:
    p = float(input("Enter the par value of a bond: "))
except ValueError:
    print("Sorry your response was not numeric. Lets assume 1000")
    p = 1000

try:
    r = float(input("Enter the interest rate of a bond: "))
except ValueError:
    print("Sorry your response was not numeric. Lets assume 4%")
    r = .04

try:
    m = float(input("Enter the maturity of the bond: "))
except ValueError:
    print("Sorry your response was not positive. Lets assume 10yrs")
    m = 10

try:
    c = float(input("Enter the coupon of the bond: "))
except ValueError:
    print("Sorry your response was not a numeric. Lets assume 5%: ")
    c = .05

pv1=p/(1+r)**m
pv2 = 0
counter = 0
while (counter < m):
    pv2 = ((p*c)/(1+r)**m)+pv2
    counter = counter + 1
else:
    print("The present value of your bond is ",pv1+pv2,".",sep="")
    
