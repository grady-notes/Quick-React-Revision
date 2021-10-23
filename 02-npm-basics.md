# NPM Basics to use React

NPM stands for `Node Package Manager`, is a package repository for the Javascript programming language which contains different packages and libraries that help in the production of effective web apps.

## npm init

- Creates a manifest file in which all the dependancies and other packages are listed. The manifest file is located in the current project directory named as `package.json`.

## npm install --save <package_name>

- Installs the specified package for the current project and keeps the details stored in the manifest file. For example if you want to install the package named axios, you will do as follows, `npm install --save axios`.

## npm install -g <package_name>

- Installs the specified package in the global package directory, so that it can be used in all projects. It requires elevation. You need to be an admin or root or a superuser for the `-g` argument to work properly.

## npm install --save-dev <package_name>

- Installs the specified package as a development dependancy and can only be used in the current development build and not in the production build.
