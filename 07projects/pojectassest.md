#Project related to DOM
##project link
[clickhere](https://stackblitz.com/edit/dom-project-chaiaurcode-w8ck7xan?file=index.html)

#solution code
##project 1
```javascript
console.log("hitesh" )
 const buttons=document.querySelectorAll('.button')
 const body=document.querySelector("body")



 buttons.forEach(function(button){
console.log(button);
button.addEventListener('click',function(e){
  console.log(e);
  console.log(e.target);
  switch(e.target.id){
    case 'grey':
    body.style.backgroundColor=e.target.id
    break;
    case 'white':
    body.style.backgroundColor=e.target.id
    break;
    case 'blue':
    body.style.backgroundColor=e.target.id
    break;
    case 'yellow':
    body.style.backgroundColor=e.target.id

  }
})
 });

```
## project 2 solution
``` javascript

const form = document.querySelector('form');

form.addEventListener('submit', function(event) {
  event.preventDefault();

  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const result = document.querySelector('#results');

  if (height === '' || height <= 0 || isNaN(height)) {
    result.innerHTML = 'Please give a valid height';
    return;
  }

  if (weight === '' || weight <= 0 || isNaN(weight)) {
    result.innerHTML = `Please give a valid weight`;
    return;
  }

  const bmi = (weight / ((height * height) / 10000)).toFixed(2);

  result.innerHTML = `<span>${bmi}</span>`;

  // ✅ BMI category
  if (bmi < 18.6) {
    console.log("Underweight");
    result.innerHTML += `<p>Underweight</p>`;
  } else if (bmi >= 18.6 && bmi <= 24.9) {
    console.log("Normal weight");
    result.innerHTML += `<p>Normal weight</p>`;
  } else {
    console.log("Overweight");
    result.innerHTML += `<p>Overweight</p>`;
  }
});


```