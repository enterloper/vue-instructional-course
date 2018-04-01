# first example:
### new Vue

```JavaScript
 new Vue({
    el: '#app',
    data: {
      text: 'Tricky Dick!!'
    }
   });
```

#### el
The element you are adding behavior to.

#### data
What we're adjusting to manage the view.

## A comparison between vanilla JavaScript and Vue.js:

Notice how much more declaritive Vue.js is.

#### VANILLA JS:
```JavaScript
const items = [
  'thingie',
  'another thingie',
  'lots of stuff',
  'yadda yadda'
];

function listOfStuff() {
  let full_list = '';
  for (let i = 0; i < items.length; i++) {
      full_list = full_list + `<li> ${items[i]} </li>`
  }
  const contain = document.querySelector('#container');
  contain.innerHTML = `<ul> ${full_list} </ul>`;     
}

listOfStuff();
```

#### HTML:
```html
<div id="container" />
```

#### VUE.js:
```JavaScript
new Vue({
  el: '#app',
  data: {
    items: [
      'thingie',
      'another thingie',
      'lots of stuff',
      'yadda yadda'
    ]
  }
});
```

#### HTML:
```html
<div id="app">
  <ul>
    <li v-for="item in items">
      {{ item }}
    </li>
  </ul>
</div>
```

#### Payoffs
- clean
- semantic
- declaritive
- legible
- easy to maintain
- reactive

