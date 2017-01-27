# psbuioffwebappservicewrker

```
function isPrime(number){
  var numArray =[];
  var this_number,divisor,not_prime;
  var this_number =3;
  while(this_number<number){
    var divisor = parseInt(this_number/2);
    var not_prime=0;
    while(divisor>1){
      if(this_number%divisor=0){
        not_prime=1;
        divisor=0;
      }else{
        divisor=divisor-1;
      }
    }
    if(not_prime==0){
      numArray.push(this_number);
    }
    this_number = this_number+1;
  }
  return numArray;
}
```

```
self.addEventListener('message',function(e){
  if(e.data.command==='start'){
    var primes = isPrime(e.data.limit);
    self.postMessage(primes);
  }
},false)
```
```
worker = new Worker('worker.js');
worker.addEventListener('message',function(e){
  output.appendChild();
  loader.
})
```


##7. Common Patterns & Practices
###2 Caching Patterns
```
event.respondWith(
  fetch(event.request).then(function(fResponse){
    return caches.open('v1').then(function(cache){
      if(!fResponse.ok){
        return cache.match(event.request);
      }else{
        cache.put(event.request,fResponse.clone());
        return fResponse;
      }
    })
  });
);
```
