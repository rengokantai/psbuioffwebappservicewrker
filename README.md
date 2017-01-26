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
