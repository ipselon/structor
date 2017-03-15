Structor - React UI Builder.
----------

[![facebook group](https://img.shields.io/badge/facebook%20group-follow-blue.svg?style=flat)](https://www.facebook.com/groups/structor/)
[![Twitter Follow](https://img.shields.io/twitter/follow/@helmetrex.svg?style=social)](https://twitter.com/helmetrex)

[![npm version](https://img.shields.io/npm/v/structor.svg?style=flat)](https://www.npmjs.com/package/structor)
[![npm downloads](https://img.shields.io/npm/dt/structor.svg?style=flat)](https://www.npmjs.com/package/structor)

Structor lets you generate scaffolds for components, containers, reducers, selectors and sagas. 
Additionally, Structor is a portal to a marketplace where you can find full-fledged React components and install their source code right into the application structure. 

You may compose/stylize a complex component using advanced UI editor and then just create the source code of a new component using sophisticated generators. 
Or you may choose to install the source code of a pre-created component into the application from marketplace.

Moreover, you have the ability to publish the source code of your component on Structor Market in order to share it or to preserve for another project.

Structor uses own Webpack Dev server to compile components, and that allows you to develop UI components in isolation from the application.  

#### What Structor is:
* **Structor is a visual editor (WYSIWYG editor)** - you may construct a React component of any complexity combining components and styling them right on the page.
* **Structor is a scaffolding tool** - you may generate scaffolds of different types of React components (dumbs, containers) with different configuration.
* **Structor is a library tool** - you may find many full-fledged components which can be installed into your project from Structor Market.
* **Structor is a playground tool** - you may modify the source code and have an instant feedback immediately because of embedded Hot Reloading tools.    

#### What Structor is not:

* Structor is not a graphical Web design tool.
* Structor is not a Web site/Web app/Web pages generator tool.
* Structor does not modify the source code of your project.

### Getting started

Stuctor can be installed in existing React projects, or in any react boilerplate projects, or even in empty folder with `package.json` file.

The only requirement is to use the following source code structures for React/Redux components in your project:    

***React components***
```
GroupName/
    ComponentName/
        index.js
```

***Redux containers***
```
GroupName/
    ComponentName/
        index.js
        actions.js
        constants.js
        reducer.js
        selectors.js
```

**Note:** Such structures are used in awesome [React Boilerplate project](https://github.com/mxstbr/react-boilerplate). 
We highly recommend to use this boilerplate as a platform of your React application. 
Here is the intro for this project: [The Hitchhikers Guide to react-boilerplate](https://github.com/mxstbr/react-boilerplate/blob/master/docs/general/introduction.md).  
 
#### Install Structor
* Run command `npm i structor`
   
After Structor is installed you will be prompted to specify the directory name where React components are. 
So Structor's Webpack will know where to find the source code of the components. 
***In case you are using React Boilerplate specify `app` name***

Additionally, you'll find a new directory in the project's root folder: `.structor`. This a metadata directory for Structor.

As far as Structor uses Webpack for compiling the source code, you will find in `.structor` dir Webpack configuration files: `webpack.base.js` and `webpack.app.js`.
The first file is used as a basic configuration and will be modified with each Structor's installation. 
The second one is created for Webpack compilation customising and will not be updated during the next install.

**Note:** The source code directory is included into Webpack config as a module dir. 
So use paths inside of this dir instead of relative paths with `../` or `./` to include components in each other:

***GOOD***
```
/**
 * SecondGroup/SecondComponent/index.js file
 */
import FirstComponent from 'FirstGroup/FirstComponent';
...

```

***BAD***
```
/**
 * SecondGroup/SecondComponent/index.js file
 */
import FirstComponent from '../../FirstGroup/FirstComponent';
...

```


#### Running Structor

1. Run `npm run structor`
1. Open in the browser Structor's workspace: `http://localhost:2222/structor`.

Now you're ready to rumble!

### First steps

#### Sign Up to Structor Market

All source code generators are available through the cloud service. You should create an account to have the access to them.
* Open main menu and select `Sign in to Stuctor Market` option.
* Click on the `Create account` link.
* Follow the instruction.

<p align="center">
  <img src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/sign-up-structor-market.png" />
</p>

#### Add component on the page (the first way)

* Click on the component on the page which will be a sibling or a parent of the new component.
* Click on one of the appending buttons (`Add Before`, `Insert First`, `Replace`, `Insert Last`, `Add After`) from the top toolbar which you may see right above the selected component.
* In the dialog type the name of a new component. (Here you may type the sequence of nested components delimited by dot)

<p align="center">
  <img src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/add-component-1.png" />
</p>

#### Add component on the page (the second way)

* Open the list of available components by clicking on the plus button.
* Click on the needed component item - it copies the component into the clipboard. 
* Select component which will be a sibling or a parent component for the component in the clipboard.
* Click on one of the appending buttons (`Add Before`, `Insert First`, `Replace`, `Insert Last`, `Add After`) from the top toolbar which you may see right above the selected component. 

<p align="center">
  <img src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/add-component-2.png" />
</p>

#### Change style of selected component on the page

* Select desired component on the page.
* Open quick options/styles panel.
* Set style option from the list.

<p align="center">
  <img src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/change-component-style.png" />
</p>

#### Scaffolding the component

* Select the component on the page.
* Click on the `New Component` button from the top toolbar of the workspace.
* Choose one of the scaffolds for components (`Scaffold generators` tab).
* Follow the wizard:
    * You may create the source code which includes all nested components into the source code. After that you will not be able to change properties of children right on the page.
    * After installation you may find new source code in `app/components/<Group>/<ComponentName>` or `app/containers/<Group>/<ComponentName>`
    * If you choose to create a Redux container you will find out that there are all bunch of needed files for Redux container: actions, constants, reducer and saga.
    * Structor is including Redux container in own Redux state which stands apart from application's Redux state. Find in `.structor/app` directory how Redux container is included into the Structor's state.  
    
<p align="center">
  <img src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/scaffolding-component-1.png" />
</p>
    
* New component will appear in the list of available components. 

<p align="center">
  <img src="https://github.com/ipselon/structor/blob/master/docs/img/scaffolding-component-2.png" />
</p>

#### Install pre-created component from marketplace

* Add empty `div` component somewhere on the page.
* Click on the `New Component` button from the top toolbar.
* Choose or search the needed component on the `All available generators`.
* Follow the wizard:
    * Some of pre-created components may inject npm dependencies. These deps will be installed after the source code is downloaded.
    * Some of pre-created components may add global imports like CSS files or additional resources. Such files will be placed into `app/assets` directory and will be imported through `.structor/app/components.js` file. These files should be injected manually into `app/app.js` file in order to use the component in your app.  
    
<p align="center">
  <img src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/install-component.png" />
</p>

#### View page structure

* Click on the code button.

<p align="center">
  <img src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/treeview-page-structure.png" />
</p>


### Useful readings

* [Structor's component model representation](https://github.com/ipselon/structor/wiki/Structor's-component-model-representation)
* [Shortcuts](https://github.com/ipselon/structor/wiki/Structor-shortcuts)

#### Tips
* To run with different port: ```structor -p <port>```<br/>
* To run in verbose mode: ```structor -v```

### License
Apache License, Version 2.0 (Apache-2.0)
