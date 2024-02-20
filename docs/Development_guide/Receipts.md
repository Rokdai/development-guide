## **TypeScript**

### Props:

If component return JSX

```tsx
interface IProps {
  prop1: type;
}

const MyComp: FC<IProps> ({prop1}) => {
  return (
    <>
    </>
  )
}
```

### Variables:

If the variable holds a boolean value: `is<Variable name>` - `isChecked`.

When a boolean value is passed, if the prop is not standard `isProp`, if the prop is standard `<Prop name>`.

Exemple: custom props - `isOpen`; standard props - `disabled`.

Import images:

```tsx
import { ReactComponent as Image } from "@assets/temp.svg";

const MyComp = () => {
  return (
    <>
      <Image />
    </>
  );
};
```
