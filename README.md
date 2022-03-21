# Python-code-
import math
print("This is a calculator which will give u the value of 'ao','an','bn' of the harmonic analysis of fourier series")
print("Note- this calculator can calculate for m=6 only")
print("Enter your value of x in degrees")
Q=input("Enter i for integer and d for degree")
if Q=="d":
    I=input("180 for period 180 degree and 360 for period 360 degree")
    x1 = int(input("X1"))
    x2 = int(input("X2"))
    x3 = int(input("X3"))
    x4 = int(input("X4"))
    x5 = int(input("X5"))
    x6 = int(input("X6"))
    print("enter your value of y")
    y1 = float(input("Y1"))
    y2 = float(input("Y2"))
    y3 = float(input("Y3"))
    y4 = float(input("Y4"))
    y5 = float(input("Y5"))
    y6 = float(input("Y6"))


    v=int(input("Enter the number of terms till which u need to print"))
    n=1
    for o in range(1,v+1):
        X1 = math.cos(math.radians(n*x1))
        p1 = round(X1, 2)
        X2 = math.cos(math.radians(n*x2))
        p2 = round(X2, 2)
        X3 = math.cos(math.radians(n*x3))
        p3 = round(X3, 2)
        X4 = math.cos(math.radians(n*x4))
        p4 = round(X4, 2)
        X5 = math.cos(math.radians(n*x5))
        p5 = round(X5, 2)
        X6 = math.cos(math.radians(n*x6))
        p6 = round(X6, 2)

        Y1 = math.sin(math.radians(n*x1))
        q1 = round(Y1, 2)
        Y2 = math.sin(math.radians(n*x2))
        q2 = round(Y2, 2)
        Y3 = math.sin(math.radians(n*x3))
        q3 = round(Y3, 2)
        Y4 = math.sin(math.radians(n*x4))
        q4 = round(Y4, 2)
        Y5 = math.sin(math.radians(n*x5))
        q5 = round(Y5, 2)
        Y6 = math.sin(math.radians(n*x6))
        q6 = round(Y6, 2)

        a = (y1 * p1)
        b = (y2 * p2)
        c = (y3 * p3)
        d = (y4 * p4)
        e = (y5 * p5)
        f = (y6 * p6)

        g = (y1 * q1)
        h = (y2 * q2)
        i = (y3 * q3)
        j = (y4 * q4)
        k = (y5 * q5)
        l = (y6 * q6)

        K = (a + b + c + d + e + f) / 3
        S=round(k,3)
        L = (g + h + i + j + k + l) / 3
        R=round(l,3)

        print("a", n, "=", S)
        print( "b", n, "=", R)
        n = n + 1

    ao = (y1 + y2 + y3 + y4 + y5 + y6) / 3
    r3 = round(ao, 3)
    print("ao=",r3)
else:
    period=int(input("enter the period"))
    p=period/2

    x1 = int(input("X1"))
    x2 = int(input("X2"))
    x3 = int(input("X3"))
    x4 = int(input("X4"))
    x5 = int(input("X5"))
    x6 = int(input("X6"))
    print("enter your value of y")
    y1 = float(input("Y1"))
    y2 = float(input("Y2"))
    y3 = float(input("Y3"))
    y4 = float(input("Y4"))
    y5 = float(input("Y5"))
    y6 = float(input("Y6"))

    v = int(input("Enter the number of terms till which u need to print"))
    n = 1
    for o in range(1, v + 1):
        X1 = math.cos((n * x1 * 3.14) / p)
        X2 = math.cos((n * x2 * 3.14) / p)
        X3 = math.cos((n * x3 * 3.14) / p)
        X4 = math.cos((n * x4 * 3.14) / p)
        X5 = math.cos((n * x5 * 3.14) / p)
        X6 = math.cos((n * x6 * 3.14) / p)

        Y1 = math.sin((n * x1 * 3.14) / p)
        Y2 = math.sin((n * x2 * 3.14) / p)
        Y3 = math.sin((n * x3 * 3.14) / p)
        Y4 = math.sin((n * x4 * 3.14) / p)
        Y5 = math.sin((n * x5 * 3.14) / p)
        Y6 = math.sin((n * x6 * 3.14) / p)

        a = (y1 * X1)
        b = (y2 * X2)
        c = (y3 * X3)
        d = (y4 * X4)
        e = (y5 * X5)
        f = (y6 * X6)

        g = (y1 * Y1)
        h = (y2 * Y2)
        i = (y3 * Y3)
        j = (y4 * Y4)
        k = (y5 * Y5)
        l = (y6 * Y6)

        K = (a + b + c + d + e + f) / 3
        Z=round(k,3)
        L = (g + h + i + j + k + l) / 3
        W=round(L,3)

        print("a", n, "=", Z)
        print("b", n, "=", W)
        n = n + 1

    ao = (y1 + y2 + y3 + y4 + y5 + y6) / 3
    R=round(ao,3)
    print("ao=", ao)

