import numpy as np


def Gaussian_elimination():
  n = int(input("Enter the length of the matrix "))
  print("Enter the values of the matrix in a single line separated by space")
  e = list(map(int, input().split()))
  A = np.array(e).reshape(n, n)

  for j in range(n):
    l = j
    while(A[l][j] == 0):
      l += 1
    if(l > n):
      print("Singular matrix")
    
    if(A[j][j] == 0):
      A[j], A[l] = A[l], A[j]
    else:
      for i in range(j+1,n):
        m = -A[i][j]/A[j][j]
        for k in range(j, n):
          A[i][k] += m*A[j][k] 
        
        y = 0
        for h in range(n):
          for u in range(n):
            A[h][u] = A[h][u]/A[y][y]
          y += 1
  
  print(A)


Gaussian_elimination()
