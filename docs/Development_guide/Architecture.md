In our architecture page is a central entity. All components, hooks, icons that are required for the particular page should be nested there. Reusable components, hooks, constants, etc. is placed in src. So folder structure may look like this.

```
src
--api
--assets
--components
--hooks
--constants
--pages
----index.tsx
----myPage
----myPage2
--store
--types
--util
```

Icons also placed in the component they are required in. If icon is requred by many components move it to assets folder.

## **Location of pictures, utilities, etc.**

If it is small and looks readable, then we put it on the same level with the component.
If more than 1, unreadable, then create folders: icons, utils, hooks, etc.

## **Component nesting**

If the component has several other components and they will be used only in it, then we create a `components` folder inside the component and put everything there.
We divide into large blocks.
If the component is reusable, then put it in the root.

## **Imports**

Do not use relative imports. Instead use absolute ones. The are listed in next.config.js

_Bad:_

```tsx
import A from "../../some-path.tsx";
```

_Good:_

```tsx
import A from "@components/some-comp.tsx";
import B from "./here.tsx";
```

```scss
@import "@assets/some-icon.png";
```
