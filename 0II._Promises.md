# Promises  :zap::zap::zap:
- Promises are ___containers___ for values that are not yet available but may eventually become available
- Promises are becoming the standard way to handle asynchronous functions in Javascript
- You start off pending and eventually the promises become either fullfill or rejected.
- Before promises, callbacks were commonly used to handle asynchronous results
- Unlike callbacks, promises are very easy to chained together

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
- The new Promise() constructor is called to create a new promise.
- The constructor takes in a callback function with the arguments ***resolve*** and ***reject***

```
    var promise = new Promise(function(resolve, reject) {
    
    });
```

## Resolve() :umbrella:
- The resolve() function is used to change the status of the promise from pending to fullfilled.
- The value that is passed inside the resolve() function becomes the fullfillment value of the promise.
- Once the resolve() function is called, future resolve() and reject() calls no longer have any effect.
ex:
  the resolve() method used here to set the fulfillment value of the promise:

```
    resolve("Success!");      //Success is set as the fulfillment value of the promise
```
## Reject() :zap: :umbrella:
- The reject() function is used to change the status of the promise from pending to rejected.
- The value that is passed inside the reject() becomes the rejection value of the promise.
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
- Both of these methods can be called outside of the new Promise() constructor.

#### Promise.resolve()  :umbrella:

```
    var resolvePromise = Promise.resolve('already resolved');
```

#### Promise.reject()   :zap:

```
    var rejectedPromise = Promise.reject('already rejected');
```

#### Resolving another Promise  :umbrella:
If another promise is passed in as an argument to resolve(), then the new promise takes the fulfillment value of the passed in Promise.

```
    var firstPromise = Promise.resolve('already resolved');
    
    var secondPromise = Promise.resolve('firstPromise');
```

:100:


  
  













