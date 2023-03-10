 # **Part 1**
 
 ![Image](CodeForStringServer.png)
 
 
 ![Image](FirstAddMessage.png)
 
 My main and HandlerRequest method was called. The relevant argument would be add message = "s". The values of this class would be "hello." The values of this request change only if the user explicitly changes the string.
 
 
 
 ![Image](SecondAddMessage.png)
 
 This second add message is essentially the same as the first added message. The arguments and the values are the same.
 
 
 # **Part 2**
 
 For lab 3, a failure-inducing input for the ReverseIn method would be {1,2,3}. The code for these inputs is the following.
 
 ```
 @Test
 public void testReversed(){
     int[] input = {1, 2, 3};
     ArrayExamples.reversed(input);
     assertArrayEquals(new int[]{3, 2, 1}, input);
 ```
 
 Its symptom is {0,0,0}. 
 
 ![Image](FirstInput.png)
 
 
 An input that doesn't induce a failure would be {1}.
 
 ```
 @Test
 public void testReversed(){
     int[] input = {1};
     ArrayExamples.reversed(input);
     assertArrayEquals(new int[]{1}, input);
 ```
 
 This would be the bug before I made the changes.
 
 ```
 static int[] reversed(int[] arr){
      int[] newArray = new int[arr.length];
      for (int i = 0; i < arr.length; i++){
          arr[i] = newArray[arr.length -i -1];
          }
          return arr;
        }
 ```
 
 This is the revised code.

 ```
 static int[] reversed(int[] arr){
      int[] newArray = new int[arr.length];
      for (int i = 0; i < arr.length; i++){
        newArray[i] = arr[arr.length - i -1];
      }
      return newArray;
    }
  ```  
  
 This new code works because in the old code, the elements in newArray are not the same as the elements in arr. In the new code, this issue is fixed.
 
 
 # **Part 3**
 
 Something I learned from lab 3 is that you can have inputs that would not produce any errors or failures, but your code would still not completely work for other inputs. This means that I have to thoroughly test my code in order to make sure that any inputs will not break my code. 
