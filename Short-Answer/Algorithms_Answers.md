Add your answers to the Algorithms exercises here.

## Exercise I


a)First line is constant (will always equal 0): O(1)
Second line is 0(n^3) because there are 3 n and they are getting multiplied together.
Last Line is 0(n^2) because there are 2 multiplication of n
Therefore second line is the dominating factor and the code is:
0(n^3)

b) First line is constant. There are 4 nested loops, each one after the first loop depends on the previous one. There for it will be (n * n * n * n). The running time will be O(n^4).

c) Takes in bunnies(n) as the range and it is a recursive function. 2nd and 3rd line of code are constants.
Last line of code is a 0(1) + 0(n-1). We can take out all constants when determining runtime. Therefore it is just 0(n).


## Excercise II

The function will take in one parameter(_n_ for number of floors). The function will divide the number of floors in half to get median value and store each half in an array. Then it will drop an egg at the middle number of the floors. If it breaks then we move to the array of lower half of the floors or if it does not break then we move to the array of higher half of the floors. Then we will run the function again for the array  that it ends up choosing.

- takes in a number of floors
- take the median value and store that number (mid)
- store the number of floors from the half to the highest floor (high)
- store the number of floors from the half to the lowest floor(low)
- condition statesment to check if eggs will break or not break in the stored number that represents the half(mid)
- if it breaks then use the function on (low)
- if it does not break then use the function on (high)
- return until the difference of the floor that breaks and floor that does not break is equal to 1.

for example function takes in 11 floors. The median value is floor 6. If it breaks on floor 6 then it will go to to floor 3. If it breaks on floor 3 it will go to floor 2. If it does not break on floor 6, it will go to floor 9. if it does not break it will go to floor 10 and if it does not break it will go to floor 11.

Runtim complexity should be 0(log n) since it is basically a binary search. Theres a sorted number of floor and you just target the  highest floor number that egg doesnt break when dropped and add 1 to it as well to return the lowest floor number that egg does break when drop.
