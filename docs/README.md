# Structor's User Guide

* [Getting Started](https://github.com/ipselon/structor/blob/master/docs#getting-started)
* [Integrating with Create React App](https://github.com/ipselon/structor/blob/master/docs/integrating-with-create-react-app.md)
* [Designing UI](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#designing-ui)
    * [A component model](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#a-component-model)
    * [Combine and modify component models](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#combine-and-modify-component-models)
       * [How to select a component](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#how-to-select-a-component)
       * [How to paste new component from library](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#how-to-paste-new-component-from-library)
       * [How to cut, copy and paste components](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#how-to-cut-copy-and-paste-components)
    * [Navigation through pages](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#navigation-through-pages)
* [Working with code](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#working-with-code)
    * [Dev environment](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#dev-environment)
    * [The code structure](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#the-code-structure)
    * [Component library](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#component-library)
       * [React components in library](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#react-components-in-library)
       * [Redux containers in library](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#redux-containers-in-library)
       * [Component default models](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#component-default-models)
    * [Generating the source code](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#generating-the-source-code)
       * [React component scaffold](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#react-component-scaffold)
       * [Redux container scaffold](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#redux-container-scaffold)
    * [Troubleshooting](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#troubleshooting)
* [Structor Market](https://github.com/ipselon/structor/blob/master/docs/structor-market.md#structor-market)
    * [Extracting and publishing components presets](https://github.com/ipselon/structor/blob/master/docs/structor-market.md#extracting-and-publishing-components-presets)
    * [Extending existing presets on the market](https://github.com/ipselon/structor/blob/master/docs/structor-market.md#extending-existing-presets-on-the-market)
* Exporting
    * Export pages
    * Export application

## Getting started

Structor does not depend on any starter/seed/boilerplate project. It even runs in an empty folder with only a `package.json`.

Before you get familiar with Structor we suggest that you run through a brief tutorial using our starter project which lets you quickly try out all of the cool features of Structor.

### Installation

* Clone or download the repo `structor-starter` from GitHub here: 

> [https://github.com/ipselon/structor-starter](https://github.com/ipselon/structor-starter).

* Run command from cloned or unpacked directory:
```
npm install
```
* Run command:
```
npm install structor
```
* When the prompt appears in the command line, choose `app` as a directory where the source code will be located.
```
Specify a directory name where the source code of the generated components will be.
If the directory does not exist in the current project structure it will be created.
(app)
```
* From this point you are able to start Structor:
```
npm run structor
```

* Open the following address in the browser:
```
http://localhost:2222/structor
```
Now you should see the Structor's workspace. If not, [please create a new issue.
](https://github.com/ipselon/structor/issues/new)
<p align="center">
  <img width="60%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/structor-workspace-first-opening.png" />
</p>

### Getting familiar with Structor's Workspace

After opening the address in the browser for the first time, you'll see the workspace page. We call it a page bacause it behaves as the real page in the browser. This page has two modes in the workspace. 

The first mode is an editing mode. In the editing mode we can cut, paste, duplicate, delete, replace, and change style of any component on the page. 

> __On a separate note__, we should understand what is a component and component model in terms of the Structor's workspace. The page in the workspace consists of multiple React components. Although the page is not a React component itself, as you may have thought, the page is just a tree of component models which are written in JSON. See a detailed explanation of what is a component model in section [A component model](https://github.com/ipselon/structor/blob/master/docs/designing-ui.md#a-component-model) of this guide.

The second mode is a preview mode. In the preview mode you are able to see how the page looks and try how it works in the browser.

On the left vertical toolbar you will find two buttons which are responsible for switching between modes:

<p align="left">
  <img width="30%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/structor-workspace-mode-switch-btns.png" />
</p>

On this stage of the tutorial the current page should be in the edit mode. If not, please enter edit mode.

### Installing component presets

While we can work in Structor with only the default components which are shipped with Structor distribution, in this tutorial we will install the [Material UI](https://github.com/ipselon/mui-next-spkg) components from [Structor Market](https://github.com/ipselon/structor-market) package.

Display the library panel by clicking on the plus icon as it is shown on the screenshot below. The library panel shows the groups of available components in the current project. Find the `Install` button at the top of the left-side panel and click on it.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-open-library.png" />
</p>

We are forwarded to the Structor Market gallery, here we can see what packages of component presets are avaialble to install. Let's install the `mui-next-spkg` package, which includes components from the next version of Material UI lib.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-install-package.png" />
</p>

Installation process will take some time because Structor installs dependencies via npm. Once the package is installed we will see new pages in the workspace and new component groups. Test out the different components using the page selector component in the top toolbar to open other pages.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-page-switcher.png" />
</p>

### Composing a new component

Let's start to compose something interesting. Make sure that the current page is set to `/home` and click on the text in the center of the page. You'll see that a border appears around the text to highlight it—it means that you selected a component. There are a several other ways find which component is currently selected.

The breadcrumb menu which appears next to the page selector menu on the right, shown in the screenshot below.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-breadcrumbs.png" />
</p>

And the more common method which shows the entire structure of the page. There is a bottom panel with the component tree of the current page. Click on the button with code icon (`</>`) on the left vertical toolbar as it is shown on the screenshot below.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-treeview-panel.png" />
</p>

> __Note__ Moving the mouse cursor around on the page will show us the boundaries of components which we are hovering over and are able to select. 

Now let's place the some components from the library onto the page.

There is a requirement in the Material UI lib to place `MuiThemeProvider` as a root component of any MUI components combination. So, we can find a `ThemeProvider` component in the `MUI` group (this is a wrapper of `MuiThemeProvider` here) and place it as a container for our future combination. 

Open the `MUI` group in the library panel and click on `ThemeProvider` item in the list. We will see that there is a sublist. The sublist in the library shows that this component has several models. Let's click on `default` model and observe that the `ThemeProvider` component's model was copied to clipboard.

Now we will replace the `h3` component in the tree with the `ThemProvider` component in the clipboard. Ensure that you have the `h3` component selected.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-add-component.png" />
</p>

Then find and click the `Replace` button in the top toolbar, or click right mouse and click the `Replace` button in the context menu.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-replace-buttons.png" />
</p>

The `Replace` button replaces the currently selected component (`h3`) with the component in our clipboard (`ThemeProvider`). The composition is shown in the screenshot below.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-component-replaced.png" />
</p>

Now replace a `Placeholder` component on the page with `raised primary` model of `Button` component. And then place `h2` component (from __HTML__ group) before `Button` inside of `LayoutItem` component. 

Placing a component before or after another component can be provided in the same manner as we were replacing components - you have to pick a component from the library and then use `Before` or `After` button in the top toolbar or context menu for selected component.

In the result we should have the following composition:

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-composed-ui.png" />
</p>

### Creating the component

Structor ships with a couple source code generators for React component scaffolds. We are not going to discuss here how it works and how it can be customized. Although, please keep in mind that any scaffold template may be changed to fit your requirements easily.

Now we are going to generate a scaffold for simple React component which will have equal look and feel as our composition which we made above.

Select the topmost `div` in the hierarchy of the current page, and click `Generate Component` button on the top toolbar of the workspace. We will see the first page of the generators gallery, where we have to choose what component we want to generate.

> __Note__: You may choose any component on the page as a root node to generate a new React component. But in this tutorial we will select the topmost one.

Here we will choose a `react-component` generator - click on `Generate` button to start a generation wizard.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-generators-list.png" />
</p>

The next step requires to enter a name of new component and/or a namespace for component.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/generators-enter-name.png" />
</p>

On this note we should step aside a bit and try to understand what the source code and its structure we will have after generation. The only requirement from Structor is to use a certain type of the source code structure. We will discuss the structure and motives to use it in the [The code structure](https://github.com/ipselon/structor/blob/master/docs/working-with-code.md#the-code-structure) guide's chapters. But on this step please keep in mind the following structure of components which is possible to use with Structor:

```
<APP_DIR>
    components/
        <COMPONENT_NAME>
            index.js - React component
    containers/
        <CONTAINER_NAME>
            index.js - Redux container
            actions.js
            constants.js
            reducer.js
            sagas.js
            selectors.js
    modules/
        <NAMESPACE_NAME>/
            components/
                <COMPONENT_NAME>
                    index.js - React component
            containers/
                <CONTAINER_NAME>
                    index.js - Redux container
                    actions.js
                    constants.js
                    reducer.js
                    sagas.js
                    selectors.js
            index.js - components and containers index
            reducer.js - composition of containers' reducers
            sagas.js - composition of containers' sagas
```

Enter `Counter` as a new name of React component, and enter `Tutorial` as a namespace. We are going to create a new namespace with `Counter` component. Although, we can create a component without any namespace and that will put it in `components` folder.

Next step gives us options for a few variants of the future scaffold. Let's leave the options as they are and proceed to the next step.

Here is a preview of the generated source code. After reviewing just click on `Install component` button.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-generated-code.png" />
</p>


Now we have to switch to the preview mode and try to click on the button - nothing happened. That is why we need to change the source code to make it something valuable.

Open `index.js` file in the directory...
```
<PROJECT_DIR>/app/modules/Tutorial/components/Counter
```

...and made chages in generated code as it is shown below. Also, please observe that your changes are applied in the preview page almost immediatelly.

```diff
/**
*
* Counter
*
*/

import React, { Component } from "react";

import PropTypes from "prop-types";

import {
  ThemeProvider,
  LayoutContainer,
  LayoutItem,
  Button
} from "modules/MUI";

const style = {
  display: "flex",
  justifyContent: "center",
  alignItems: "center",
  padding: "1em"
};

class Counter extends Component {
  constructor(props) {
    super(props);
++    this.handleIncrease = this.handleIncrease.bind(this);
    this.state = {
--      exampleValue: ""
++      counterValue: 0, 
    };
  }

++  handleIncrease(e) {
++    e.stopPropagation();
++    e.preventDefault();
++    this.setState({counterValue: this.state.counterValue + 1});
++  }

  render() {
--    const { exampleValue } = this.state; // eslint-disable-line
--    const { exampleProp } = this.props; // eslint-disable-line
++    const {counterValue} = this.state; // eslint-disable-line
    return (
      <div style={style}>

        <div>
          <ThemeProvider>
            <LayoutContainer gutter={24}>
              <LayoutItem xs={12}>
--                <h2><span>Empty h2</span></h2>
++                <h2><span>Count: {counterValue}</span></h2>
--                <Button raised={true} primary={true}>
++                <Button 
++                  onClick={this.handleIncrease} 
++                  raised={true} 
++                  primary={true}
++                >
                  <span>Button</span>
                </Button>
              </LayoutItem>
            </LayoutContainer>
          </ThemeProvider>
        </div>

      </div>
    );
  }
}

-- Counter.propTypes = {
--   exampleProp: PropTypes.string
-- };
-- Counter.defaultProps = {
--   exampleProp: ""
-- };

export default Counter;
```

Switch again to the preview mode and try to click on the button - you will see that the counter value is increasing.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-component-preview.png" />
</p>

### Exporting pages and building App

This step is not necessary to the projects which have own building process and requre to add components manually into appliation pages. Structor Starter App does not have a sophisticated app building process in terms of granularity, optimisation, etc. This step is mostly for the learning purpose.

Click on the button with book icon on on the left vertical toolbar. This will show us a list of available pages.

In the top of the list we may see two buttons: `Export Pages` and `Export App`. `Export Pages` responsible for generating the source code for selected pages. And `Export App` button generates not only the pages' source code, but also the source code for entry point in terms of Webpack compiler.

<p align="center">
  <img width="70%" src="https://raw.githubusercontent.com/ipselon/structor/master/docs/img/first-tutorial-export-app.png" />
</p>

As far as we are going to build application, we are choosing `Export App`. The modal dialog will worn us about what files will be generated.

After we will see a green message about a successful exporting. Now we can find a new `<APP_DIR>/routes` folder along with files for React/Redux application. Additionally, please find the compiled bundle of the application in `<PROJECT_DIR>/build` directory.

Finally we can run our application in the local Express server, go to the terminal and run following command:
```
npm run start:production
```

This command initiates a building process of our application and starts an Express server instance on `3000` port. After the server is started we may open `http://localhost:3000` address in our browser.



