# EX-NO-9A-linear-trend-estimation
## AIM:
   To implement a linear trend estimation using python program 
## PROCEDURE:
   1.Import Required Libraries
   
   2 Calculate the sum of the elements in array x and y
   
   3 Calculate b using the formula for linear regression.
   
   4 Calculate the mean of X and Y values and store them in meanX and meanY.
   
   5.The final output includes the regression line equation and a plot of the data with the regression line.

## PROGRAM:
```
def calculateB(x, y, n):

    # sum of array x
    sx = sum(x)

    # sum of array y
    sy = sum(y)

    # for sum of product of x and y
    sxsy = 0

    # sum of square of x
    sx2 = 0

    for i in range(n):
        sxsy += x[i] * y[i]
        sx2 += x[i] * x[i]
    b = (n * sxsy - sx * sy)/(n * sx2 - sx * sx)
    return b

# Function to find the
# least regression line
def leastRegLine(X,Y,n):

    # Finding b
    b = calculateB(X, Y, n)
    meanX = int(sum(X)/n)
    meanY = int(sum(Y)/n)

    # Calculating a
    a = meanY - b * meanX
    m = meanX
    # Printing regression line
    print("Regression line:")
    print("Y = ", '%.3f'%a, " + ", '%.3f'%b, "*X", sep="")

X=np.array(eval(input()))
Y=np.array(eval(input()))
n = len(X)
leastRegLine(X, Y, n)
print (m,a)
Y_pred=m*X+a
print (Y_pred)
plt.scatter (X,Y)
plt.title('Regression')
plt.xlabel('X_Values')
plt.ylabel('Y_Values')
plt.plot(X,Y_pred, color="red")
plt.show()








```
## OUTPUT:



![image](https://github.com/praveenst13/EX-NO-9A-linear-trend-estimation/assets/118787793/afd20999-1725-4fe2-b615-7e35dd93043f)




## RESULT :
  Thus the program to implement a linear trend estimation is written and verified using python programming.
