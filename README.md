# rankNull
A small program for finding the rank and nullity of any matrix size 99x99 or less.
Here is some explanation:

rref([A])->[A] This takes the matrix [A], row reduces it, and stores the row reduced version into the matrix [A]. It replaces [A] with it's row reduced version.

dim([A])->L1 This stores the dimensions of [A] into a list, L1.

0->R This stores the value zero into R. R counts how many zero rows there are in [A].

For(A,1,X) This starts a loop. It counts from 1 to X, X being the number of rows in [A], with A as my incrementing variable.

rowSwap([A],1,A)->[A] This swaps the first row of [A] with the position of A in the current iteration. There is no way to select a row specifically, and since it's doing this for a matrix of any size, this was the best alternative I could think of.

Matr>list([A]T,L2) Then store the first row of [A] transpose (which has been swapped for the row at the value of A) into list two, L2. This built in function stores
the column of a matrix to a corresponding list variable, so I had to use the transpose to make sure L2 gets the row of [A].

If (sum(L2)=0) Then it checks if the sum of L2 is zero. If all the values of it are zero I proceed to the next step which...

R+1->R ...increments the variable R by one.

End End the loop.

X-R→Z This stores the rank into the variable Z.

Disp "Rank A" Tell the user what to expect.

Disp Z Displays Z.

Disp “Nullity” Tells the user what to expect.

L1(2)-Y This stores the column number into the variable Y.

Disp Y-Z This subtracts the Column number from the rank to get the nullity.

I made a short video testing the program with three problems from chapter 4.6. I have not found a matrix for which this fails, even mxn matrices work, though I am not sure for all cases. Definitely for all cases of nxn matrices it will work though.
If you don’t understand it read up on the documentation for TI-BASIC. http://tibasicdev.wikidot.com/home

https://streamable.com/2eptv
