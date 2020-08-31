# Deploying a New React App with GitHub Pages

[A fresh react app, deployed to GitHub pages for free!][pagelink]

#### Create a new React App
```
npx create-react-app react-ghpages
cd react-ghpages
```

#### Install Github pages dependency
```
npm install gh-pages --save-dev
```

#### *Inside Package.Json*: Add the homepage link before *name*
```
{
  "homepage": "http://TimothyFHinds.github.io/react-ghpages",
  "name": "react-ghpages",
  ..
```

#### *Inside Package.Json*: Add new scripts for deployment
```
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build",
  ..
```

#### *Inside .gitignore*: Remove /build 

#### [Create a *Public* GitHub Repository][newrepo]

#### Link to your GitHub Repository
```
git init
git remote add origin git@github.com:TimothyFHinds/react-ghpages.git
```

#### Commit, deploy and push your code
```
git add *
git commit -m "init commit"
npm run deploy
git push -u origin master
```

#### You can find the link to the site within your Repository Settings Page

[newrepo]: https://github.com/new
[pagelink]: https://timothyfhinds.github.io/react-ghpages/
