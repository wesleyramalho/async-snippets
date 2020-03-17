# Dealing with asynchronous code with JS
Asynchronous code snippets in JavaScript

## Async and Await example

```javascript
async function getUserAsync(name) 
{
  let response = await fetch(`https://api.github.com/users/${name}`);
  let data = await response.json()
  return data;
}

getUserAsync('wesleyramalho')
  .then(data => console.log(data));

```


## Using Promises API

```javascript
function getUser(name){
 fetch(`https://api.github.com/users/${name}`)
  .then(function(response) {
    return response.json();
  })
  .then(function(json) {
    console.log(json);
  });
};

//get user data
getUser('wesleyramalho');

```



Reference:
[Fetch API using async await](https://dev.to/shoupn/javascript-fetch-api-and-using-asyncawait-47mp)

