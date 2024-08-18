Numpy arrays are multidimensional. It considers python lists as arrays.

**reshape() in numpy:**

arr1 = np.array(np.random.randint(10,45,(3,8))) # Its shape is 3,8
Now I can reshape it into any dimensional but the deimension sould be divisible by 3*8 i.e. 24
possible reshape options considering any dimensions are : (1,24), (2,12), (1,2,12), (4,6),(4,1,1,6) etc.
Now if there is an -ve number in the shape then it'll first consider the other positive dimenion and make this -ve number to the rest +ve dimenion. For the above case if new shape is (2,-1,12) the after operation the new dimension of the array will be = 2,1,12

(2,-1,4) will be = (2,3,4)

<img width="220" alt="image" src="https://github.com/GrowingStone07/python/assets/106248741/cca3b1d5-dc6b-441d-874d-37a6f697688d">
