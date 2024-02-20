To add css one may use 2 ways:

1. Create an ordinary `scss` file and import it like this:

```tsx
import "./my-css.scss";

const Comp = () => {
  return null;
};
```

2. Create a `*.module.scss` file to use css-modules (prefered):

```tsx
import styles from "./my-css.m.scss";

const Comp = () => {
  return <div className={styles.myClass}></div>;
};
```

This way you may safely use short class names like `.btn`, `.item` or whatever you want, because your classname after build will be transformed to unique one. Read more on css-modules: https://github.com/css-modules/css-modules

Try to avoid using id selectors and !important. The best variant is a simple class without nesting.

## **Style grouping**

Styles are broken down into meaningful blocks and separated by a space line.

First come all styles related to positioning and alignment of the element. Then, width and height styles. After that, indents, etc.

Exemple:

```scss
.empty {
  display: flex;
  justify-content: center;
  align-items: center;

  width: 100%;
  height: 100%;

  font-size: 16px;
  line-height: 22px;

  color: $default-text;
}
```
