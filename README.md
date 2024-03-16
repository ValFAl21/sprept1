#sprept1
#Code for division, fix later
def add(a, b):
    return a + b

def subtraction(a, b):
    return a - b
   
def multiplication(a, b):
    return a * b

def division(a, b):
    try:
        split = a / b
    except TypeError:
        split = "Error"
    print(split)

#Code for frac, sq roots, and the power of (done w this part)
import math

def squareroot(a): #sq roots
    return math.sqrt(a)

def squared(a):
    return a ** 2

def root(n, a):
    result = a ** (1/n)
    return result

def power(a, n):
    result = a ** n
    return result

def mod(a, b):
    remainder = a % b
    return(remainder)
   
#part_2 of calc
import math
def sinr(x):
    return math.sin(x)
   
import math
def sind(x):
    return math.sin(math.radians(x))
   
import math
def cosr(x):
    return math.cos(x)
   
import math
def cosd(x):
    return math.cos(math.radians(x))
   
import math
def tanr(x):
    return math.tan(x)
   
import math
def tand(x):
    return math.tan(math.radians(x))
   
import math
def asinr(x):
    return math.asin(x)
   
import math
def asind(x):
    x_radians = math.radians(x)
    return math.asin(x_radians)

import math
def acosr(x):
    return math.acos(x)
   
import math
def acosd(x):
    x_radians = math.radians(x)
    return math.acos(x_radians)

import math
def atanr(x):
    return math.atan(x)
   
import math
def atand(x):
    x_radians = math.radians(x)
    return math.atan(x_radians)

import math
def mean(x):
    if len(x) == 0:
        return 0
    return sum(x) / len(x)
 
import math  #check this one later
def mode(x):
    freq = {}
    for num in x:
        if num in freq:
            freq[num] += 1
        else:
            freq[num] = 1
    max_freq = max(freq.values())
    modes = [key for key, value in freq.items() if value == max_freq]
    return modes

import math
def median(x):
    sorted_x = sorted(x)
    n = len(sorted_x)
    if n % 2 == 0:
        mid_1 = sorted_x[n//2 - 1]
        mid_2 = sorted_x[n//2]
        return (mid_1 + mid_2) / 2
    else:
        return sorted_x[n//2]

import math
def sum(x):
    total = 0
    for i in x:
        total += i
    return total
   
import math
def fq(x):
    n = len(x)
    q1_index = math.ceil(0.25 * (n+1)) - 1
    sorted_x = sorted(x)
    return sorted_x[q1_index]
   
import math
def tq(x):
    n = len(x)
    q3_index = math.ceil(0.75 * (n+1)) - 1
    sorted_x = sorted(x)
    return sorted_x[q3_index]
   
import math
def iqr(x):
    sorted_x = sorted(x)
    n = len(sorted_x)
   
    q1_index = math.ceil(0.25 * (n+1)) - 1
    q3_index = math.ceil(0.75 * (n+1)) - 1
   
    q1 = sorted_x[q1_index]
    q3 = sorted_x[q3_index]
   
    iqr = q3 - q1
    return iqr
   
import math
def stdev(x):
    n = len(x)
    mean = sum(x) / n
    variance = sum ((xi - mean) ** 2 for xi in x) / n
    std_dev = math.sqrt(variance)
   
    return std_dev

#part 3 of calc
import numpy
import matplotlib.pyplot
def plot2p(x1, x2, y1, y2):
    x_values = [x1, x2]
    y_values = [y1, y2]
    plt.plot([x_values, y_values)
    plt.xlabel("X")
    plt.ylabel("Y")
    plt.title("Line between two points")
    plt.show()
