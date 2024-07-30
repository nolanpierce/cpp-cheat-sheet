# SEARCHING FUNCTIONS

## std::binary_search(beginning index, ending index, value we want to check if is inside container eg.(4));
** PARAMS **
- beginning index : it is the start of the conatiner(array etc...) we are searching for so we would start at 0 of our array the first index but you can also start at the middle or anywhere except the end
- ending index : i think if you read the top you get the gyst here but it should be one element(value in array) past the element in range so one past the index we are wanting so if we are using vectors we can go vec.end() but if we are wanting to go to the middle we would do something like vec.begin() + 4(the index we are wanting)
- value : is the value or element we are searching for in our array

** What does it return **
It will return a boolean true or false if it is found it will return true if it isnt it will return false so use this as a way to verify it is inside of the array like a check if somebody is home when u knock on their door if not then u cannot enter or do anything

** Behind the hood of the function **
It checks if a value is stored inside the container we are giving it and like i said it returns if it is found or not

** Code example **
```cpp

  if( std::binary_search(vec.begin(), vec.end(), 4)){
      std::cout << "Found our value we can proceed\n";
  }

```

## std::find(beginning index, ending index, value we want get);
** PARAMS **
- beginning index : it is the start of the conatiner(array etc...) we are searching for so we would start at 0 of our array the first index but you can also start at the middle or anywhere except the end
- ending index : i think if you read the top you get the gyst here but it should be one element(value in array) past the element in range so one past the index we are wanting so if we are using vectors we can go vec.end() but if we are wanting to go to the middle we would do something like vec.begin() + 4(the index we are wanting)
- value : is the value or element we are searching for in our array

** What does it return **
It will return the furst occurance of the value in our container, so make sure this is sorted before and its something that doesnt need to be specific i normally will use this for unordered_sets because there literally is no other occurance of our value but still can be used just rememeber that.

** Behind the hood of the function **
Searches for the first occurance of the value in the vector or container and returns its iterator if it doesnt find the value it will default return the end of the conatiner

** Code example **
```cpp

  auto it = std::find(vec.begin(), vec.end(), 3);
  if(it != vec.end()){
    std::cout << "Found our value : "  << *it << "\n";
  }

```
