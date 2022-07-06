# How To Create Color Theme

## Requirements
* Git
* Node.JS
* npm
* yo
* generator-code
* vsce
* [Azure DevOps Account](https://dev.azure.com/)

## Setup
```
npm install -g yo generator-code

yo code
```

1. Select New Color Theme
1. Select No, start fresh
1. Enter the name of your extension
1. Enter your extension identifier (ex. of what a identifier is: {publisher-name}.{identifier} | just press enter and use the default)
1. Write a short description of what the theme represents or what the idea behind the theme is.
1. Enter the name (case sensitive) as you want it to appear in the marketplace (This is the extension display name)
1. Select a base theme to be used as a starting point

```
cd {theme-name}
code .
```

## Usage
To test your theme, press `F5` and select `Theme` from the menu.

## Publishing
```
npm install vsce -g
```

* Create Git Repo on GitHub
* Push code then edit JSON

### Azure DevOps
* Create an Organization
* Create Personal Access Token
  * Use "All Accessible Organizations"
* [Create Publisher](https://marketplace.visualstudio.com/manage/createpublisher)
```
vsce login (publisher name)
vsce package
vsce publish

vsce publish minor
```
