# dicas
## Components 
Components are the building blocks of React applications. 
They let us split the UI into independent, reusable pieces, and think about each piece in isolation.

>React apps are made out of components
>
>A component can be as small as a button, or as large as an entire page.

```javascript
function MyButton() {
  return (
    <button>I'm a button</button>
  );
}

```
Now that you’ve declared MyButton, you can nest it into another component:

```javascript
export default function MyApp() {
  return (
    <div>
      <h1>Welcome to my app</h1>
      <MyButton />
    </div>
  );
}
```
### Displaying data:
JSX lets you put markup into JavaScript. Curly braces let you “escape back” into JavaScript 
so that you can embed some variable from your code and display it to the user. 
For example, this will display user.name:

```javascript
return (
  <h1>
    {user.name}
  </h1>
);
```

```javascript
const user = {
  name: 'Hedy Lamarr',
  imageUrl: 'https://i.imgur.com/yXOvdOSs.jpg',
  imageSize: 90,
};
```

### Conditional rendering:
In React, there is no special syntax for writing conditions. 
Instead, you’ll use the same techniques as you use when writing regular JavaScript code. 
For example, you can use an if statement to conditionally include JSX:


### Rendering list:

You will rely on JavaScript features like for loop and the array map() function to render lists of components.
For example, let’s say you have an array of products:

```javascript
cconst products = [
  { title: 'Cabbage', id: 1 },
  { title: 'Garlic', id: 2 },
  { title: 'Apple', id: 3 },
];
```

Inside your component, use the map() function to transform an array of products into an array of l1 items:

<span style="color: red;">????

```javascript
const listItems = products.map(product =>
  <li key={product.id}>
    {product.title}
  </li>
);

return (
  <ul>{listItems}</ul>
);
```
