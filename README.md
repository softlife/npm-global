# npm-global
Node script for installing packages globally for multiple application development.

## DESCRIPTION

In a .NET development environment of many web application products migrating to AngularJS/Bootstrap, the developers were routinely working on multiple product releases. A common method was required for initializing the product development environment without having to install the same Node packages (gulp, bower, etc.) several times on the same machine.

I wanted the tool to meet these requirements:

1. Installation of Node and Git as the only prerequisite.
2. "npm install" command should install the global Node development environment as well as all locally required packages for any release of any product under development.
3. Global packages should be installed only if not already installed.
4. Local links to global packages must be created automatically.

## USAGE

Install ``npm-global.js`` to a folder of common development resources available to all developers and modify ``packages`` object  to include the desired Node packages to be installed.

Create or modify ``package.json`` in the development root folder of any product to include the following:
```javascript
"scripts":
  {
  "preinstall" : "node CommonResourcesFolder/npm-global.js links"
  }
```
- ``links`` parameter will create links in the local ``node_modules`` folder to the globally installed packages.

Run `npm install` to install all the global packages. 



## AUTHORS

* Steve Thames (@sthames42)
