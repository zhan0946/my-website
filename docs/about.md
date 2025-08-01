# About
This website is a space for you to learn and practice JavaScript. The live editor runs your code right away without the need to install any development environments.

## Try it now
```jsx live
function Greeting() {
  return (
    <h2>Hello world!</h2>
  )
} 
```

## Sample snippets
Copy one of the code snippets below and paste it into the editor to see what happens.

```js
///////////////////// EXAMPLE 1. BUTTON THAT SAYS HEY /////////////////////
function MyPlayground(props) {
  return (
    <div>
      <button onClick={() => alert('hey!')}>Click me</button>
    </div>
  );
}

///////////////////// EXAMPLE 2. WORKING CLOCK /////////////////////
function Clock(props) {
  const [date, setDate] = useState(new Date());
  useEffect(() => {
    const timerID = setInterval(() => tick(), 1000);

    return function cleanup() {
      clearInterval(timerID);
    };
  });

  function tick() {
    setDate(new Date());
  }

  return (
    <h3>It is {date.toLocaleTimeString()}</h3>
  );
}
```

*Code snippets courtesy of [Docusaurus](https://docusaurus.io/docs/markdown-features/code-blocks).*