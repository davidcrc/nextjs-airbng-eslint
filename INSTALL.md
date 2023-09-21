## Setup

- When run create-next-app:

```
Would you like to use TypeScript?  Yes
Would you like to use ESLint?  Yes
Would you like to use Tailwind CSS?  Yes
```

### Add prettier

```bash
yarn add --dev --exact prettier
```

or

```bash
npm install --save-dev --save-exact prettier
```

- create .prettierrc.json, you can add more otions if you want:

```json
{
  "singleQuote": true
}
```

### Add prettier for tailwind ( Tailwind CSS classes name will be sorted)

```bash
yarn add --dev prettier prettier-plugin-tailwindcss
```

or

```bash
npm install --save-dev prettier prettier-plugin-tailwindcss
```

- Update .prettierrc.json:

```json
{
  "singleQuote": true,
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

### Add ESlint with airbnb's rules

```bash
npx install-peerdeps --dev eslint-config-airbnb
```

- Update .prettierrc.json:

```json
{
  "extends": ["airbnb", "airbnb/hooks", "next/core-web-vitals"]
}
```

- now for this error: "JSX not allowed in files with extension '.tsx'"

```bash
yarn add eslint-config-airbnb-typescript \
  @typescript-eslint/eslint-plugin \
  @typescript-eslint/parser \
  --dev
```

or

```bash
npm install eslint-config-airbnb-typescript \
  @typescript-eslint/eslint-plugin@^6.0.0 \
  @typescript-eslint/parser@^6.0.0 \
  --save-dev
```

- Update .prettierrc.json:

```json
{
  "extends": [
    "airbnb",
    "airbnb-typescript",
    "airbnb/hooks",
    "next/core-web-vitals"
  ],
  "parserOptions": {
    "project": "./tsconfig.json"
  }
}
```

- Integrate Prettier with ESlint

```bash
yarn add --dev eslint-config-prettier
```

or

```bash
npm install --save-dev eslint-config-prettier
```

- Update .prettierrc.json:

```json
{
  "extends": [
    "airbnb",
    "airbnb-typescript",
    "airbnb/hooks",
    "next/core-web-vitals",
    "prettier"
  ],
  "parserOptions": {
    "project": "./tsconfig.json"
  }
}
```
