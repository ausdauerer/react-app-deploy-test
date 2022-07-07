# react-app-deploy-test

### React app to test the deployment of react apps on github.io

## Steps to deploy

1. Create Repository and publish it to github
2. Add a react app
3. Add homepage url to package.json
```
{
  "name": "my-app",
  "version": "0.1.0",
+ "homepage": "https://{username}.github.io/{repositoty-name}",
  "private": true,
```
4. Add scripts to package.json
```
"scripts": {
+   "predeploy": "npm run build",
+   "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
```
5. Finally run command ```npm run deploy``` to build and deploy
