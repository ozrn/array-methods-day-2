# JS30 #7: array-methods-day-2
This is yet another coding challenge from JS30 series by Wes Bos.<br>
This project shows how to use a couple of array methods like some, every and find etc.<br><br>
### The some method
It checks if any array element passes the test by the provided function or not.<br>
It returns true if the callback function returns a truthy value for at least one element in the array. Otherwise, it returns false.<br>
In this step, this method is used to test if there is any person who is 19 or older.
```
const isAdult = people.some(person => ((new Date()).getFullYear()) - person.year >= 19);
```
### The every method
It checks if every single element passes the test by the provided function or not. In order to return true, the callback function<br> 
needs to return truthy for each array element. Otherwise, it returns false.<br>
In this step, whether all people are 19 or older in the given array is tested.
```
const allAdults = people.every(person => ((new Date()).getFullYear()) - person.year >= 19);
```
### The find and findIndex methods
The find method returns the first element that passes a test whereas the index of the first element passing a test is found using findIndex.<br>
Here, in this step, the first one is used to find the comment with the ID of 823423.
```
const comment = comments.find(comment => comment.id === 823423);
```
### The slice method
It returns a new array containing the selected elements from start to end ( end not inclusive). Start and end are the indexes of the items.<br><br>
In the last challenge, both findIndex and slice methods are applied to delete the comment with the ID of 823423. First, the index of that comment is found
and then deleted using these methods respectively.
```
const index = comments.findIndex(comment => comment.id === 823423);
   const newComments = [
      ...comments.slice(0, index),
      ...comments.slice(index + 1)
    ];
```


