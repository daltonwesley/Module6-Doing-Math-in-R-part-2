# Module6-Doing-Math-in-R-part-2
During this assignment, I had to learn how to use R to create the following matrix.




# Before I could make the matrix I had to practice the proper coding with the following example.

1. Consider A=matrix(c(2,0,1,3), ncol=2) and B=matrix(c(5,2,4,-1), ncol=2).
a) Find A + B
b) Find A - B

   # First I cleaned up the layout of the text to look like this.

A=matrix(c(2,0,1,3), ncol=2) 
B=matrix(c(5,2,4,-1), ncol=2)
A + B
A - B

# After running the addiction/substraction command, I got the following
> A + B
     [,1] [,2]
[1,]    7    5
[2,]    2    2

> A - B
     [,1] [,2]
[1,]   -3   -3
[2,]   -2    4


   # For part 2, I was told to make a matrix for using the diag() function to build a matrix of size 4 with the following values in the diagonal 4,1,2,3. The way I accomplished this is by using the command 

> diag(c(4,1,2,3))
     [,1] [,2] [,3] [,4]
[1,]    4    0    0    0
[2,]    0    1    0    0
[3,]    0    0    2    0
[4,]    0    0    0    3

   # For the main question, I had to make a 5x5 matrix so with the number 3 running diagonally so I used the C <- diag(rep.int(3, 5)). This command allows me to repeat "3" 5 times. 
# The command (rep.int(,)) understands that the first number "3" is the integer and the next number "5" is the number of times it will be repeated diagonally. 

     [,1] [,2] [,3] [,4] [,5]
[1,]    3    0    0    0    0
[2,]    0    3    0    0    0
[3,]    0    0    3    0    0
[4,]    0    0    0    3    0
[5,]    0    0    0    0    3

   # Now that I these number set I needed to get "1" to run cross the [1,] row. So I did that by using the command > C[1,2:5] <- rep.int(1, 4) . This command, C[1,2:5] will place the number "1" in column 2-5 and repeat the integer "1" 4 times

     [,1] [,2] [,3] [,4] [,5]
[1,]    3    1    1    1    1
[2,]    0    3    0    0    0
[3,]    0    0    3    0    0
[4,]    0    0    0    3    0
[5,]    0    0    0    0    3

   # Lastly, I needed to place the number "2" down the first column of all the rows. The way I accomplished this is through the command, > C[2:5,1] <- rep.int(2, 4). As seen in the previous step the same rules apply. 


     [,1] [,2] [,3] [,4] [,5]
[1,]    3    0    0    0    0
[2,]    2    3    0    0    0
[3,]    2    0    3    0    0
[4,]    2    0    0    3    0
[5,]    2    0    0    0    3

  # This is how I was able to create the matrix given in this assignment. The following code is below

A=matrix(c(2,0,1,3), ncol=2) 

B=matrix(c(5,2,4,-1), ncol=2)

A + B

A - B

diag(c(4,1,2,3))

C <- diag(rep.int(3, 5))

C[1,2:5] <- rep.int(1, 4)

C[2:5,1] <- rep.int(2, 4)

C

