# Promises  :zap::zap::zap:
- Promises are ___containers___ for values that are not yet available but may ___eventually___ become available
- Promises are becoming the ___standard___ way to handle ___asynchronous___ functions in Javascript
- You start off pending and eventually the promises become either ___fullfill___ or ___rejected___.
- Before promises, callbacks were commonly used to handle asynchronous results
- Unlike callbacks, ___promises are very ___easy___ to ___chained___ together

## Creating a new Promise :umbrella:

```
    var promise = new Promise(function(resolve, reject) {
        
        //do stuff
        
        var isSuccessful = true;
        
        if(isSuccessful) {      //if everything is successful
          resolve("Success!");
        }
        else {                  //if something went wrong
          reject(Error('Failure'));
        }
        
        
    }); //promise

```

## new Promise() :zap:
- The ___new Promise() constructor___ is called to create a ___new promise___.
- The constructor takes in a callback function with the arguments ***resolve*** and ***reject***

```
    var promise = new Promise(function(resolve, reject) {
    
    });
```

## Resolve() :umbrella:
- ___The resolve() function___ is used to ___change___ the ___status___ of the promise from pending to fullfilled.
- The ___value___ that is passed inside the resolve() function becomes the ___fullfillment___ value of the promise.
- Once the resolve() function is called, future resolve() and reject() calls no longer have any effect.
ex:
  the resolve() method used here to set the fulfillment value of the promise:

```
    resolve("Success!");      //Success is set as the fulfillment value of the promise
```
## Reject() :zap: :umbrella:
- ___The reject() function___ is used to ___change___ the ___status___ of the promise from pending to rejected.
- The ___value___ that is passed inside the reject() becomes the ___rejection___ value of the promise.
- Once the reject function is called, future resolve() and reject() calls no longer have any effect.
- The resolve function can take in any object as an argument, but one common practice is to pass in a ***Error*** object
  because it provides a more detailed error report.
ex:
  the reject() method is used to send an Error object as its reject value:
  
  ```   
    reject(Error('failure'));   //rejection value becomes an Error object
  
  ```
 
### Promise.resolve() and Promise.reject()  :zap: :umbrella:
- Promise.resolve() is used to return a promise that is already fulfilled.
- Promise.reject() use to return a promise already rejected
- ___Both___ of these methods can be ___called outside___ of the new Promise() ___constructor___.

#### Promise.resolve()  :umbrella:

```
    var resolvePromise = Promise.resolve('already resolved');
```

#### Promise.reject()   :zap:

```
    var rejectedPromise = Promise.reject('already rejected');
```

#### Resolving another Promise  :umbrella:
If __another promise is passed__ in as an argument to resolve(), __then__ the __new promise__ takes the fulfillment __value__ of the __passed__ in Promise.

```
    var firstPromise = Promise.resolve('already resolved');
    
    var secondPromise = Promise.resolve('firstPromise');
```

:100:


  
  













