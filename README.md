## TypeScript Node Project Setup
https://khalilstemmler.com/blogs/typescript/node-starter-project/


---

### Eslint
```sh
npm install --save-dev eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin

touch .eslintrc

touch .eslintignore

```
plugin
```sh
npm install --save-dev eslint-plugin-no-loops
```

---

### Prettier
https://khalilstemmler.com/blogs/tooling/prettier/

```sh
npm install --save-dev prettier
touch .prettierrc
```
Formatting using VSCode on save
```json
"editor.formatOnPaste": true,
"editor.formatOnSave": true,
```

Formatting using an filesystem watcher
```sh
npm install --save-dev onchange
```

Configuring Prettier to work with ESLint
```sh
npm install --save-dev eslint-config-prettier eslint-plugin-prettier

```

---

### Hasky
https://typicode.github.io/husky/

```sh
npm install husky --save-dev

# enable Git hooks
npx husky install

```
Automate Git hooks
`package.json`
```sh
npm pkg set scripts.prepare="husky install"
```
create a pre-commit hook
```sh
npx husky add .husky/pre-commit "npm run lint"

git add .husky/pre-commit
```

