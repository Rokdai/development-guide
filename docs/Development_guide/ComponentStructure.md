The structure of the component should look as follows

```tsx
const Comp = () => {
  const [data, setData] = useState(null);
  /*
    working with state, getting data from hooks, etc.
    */

  const onChange = () => {};
  /*component methods description*/

  useEffect(() => {}, []);
  /*effect manipulation*/

  return; /*component markup*/
};
```

If possible, you should avoid calling dynamically modified methods/content when rendering a component, as this can lead to unexpected re-rendering
