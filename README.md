# Carbon Tutorial for NextJS 13

Base NextJS 13 app using IBM Carbon Design System React components

## Create NextJS 13 app

```bash
yarn create next-app

✔ What is your project named? … next-base
✔ Would you like to use TypeScript? … *No / Yes
✔ Would you like to use ESLint? … No / *Yes
✔ Would you like to use Tailwind CSS? … *No / Yes
✔ Would you like to use `src/` directory? … No / *Yes
✔ Would you like to use App Router? (recommended) … No / *Yes
✔ Would you like to customize the default import alias? … *No / Yes

cd carbon-tutorial-next
yarn dev
```

Configure paths in `jsconfig.json`

```
{
  "compilerOptions": {
    "baseUrl": "./src",
    "paths": {
      "@/components/*": ["components/*"],
      "@/app/*": ["app/*"]
   }
  }
}
```

## Update the NextJS Bootstrap

Modify some of the boostrap code in order to support the Carbon components.

In `app/layout.js` (RootLayout) take out:

```
import { Inter } from 'next/font/google'
const inter = Inter({ subsets: ['latin'] })
```

Take out className tag from <body> and update the meta data.

Then `yarn dev` to confirm.
