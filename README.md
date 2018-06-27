# App Store Widget Boilerplate

This boilerplate gives you all you need to start a new custom widget for Mendix
5.6.0 and up.

The boilerplate contains:
- Directory structure
- Readme.md
- License
- JavaScript source
- XSD for package.xml, to configure properties of the widget, visible inside the
 Mendix business modeler

## Contributing

For more information on contributing to this repository visit [Contributing to a GitHub repository](https://world.mendix.com/display/howto50/Contributing+to+a+GitHub+repository)!

## Typical usage scenario

Use this template to start building a widget for Mendix 5.
Alter this README.md file and describe what your widget does.
 
## Description

The javascript inside the widget has examples of:
- Using CSS within a widget
- Using templating
- Loading external library's
- DOM manipulation
- Event attaching
- Loading data
- Executing microflow and sending data
- Working with the context object, which is an object in the current context
(e.g. the one displayed in a DataView).

### Dojo AMD module list

The JavaScript contains an extensive list of modules that may be used to build a
widget. It is best to reduce this list to what is actually used. Use JSHint to
help identify errors and problems. 

** Be sure to keep the module name array and the parameter list of the anonymous
function below the module list in sync! **

The following modules are necessary for all widgets:
- dojo/_base/declare
- mxui/widget/_WidgetBase
- dijit/_Widget

If your widget does not use an HTML template:
- Remove dijit/_TemplatedMixin from the module list
- Remove _Templated from the parameter list of the anonymous function below the module list
- Remove _Templated from the parameter list of the declare call
- Remove the templates folder

If your widget does not need jQuery:
- Remove WidgetName/widget/lib/jquery from the module list
- Remove _jQuery from the parameter list of the anonymous function below the module list
- Remove _jQuery from the parameter list of the declare call
- Remove jquery.js from src\WidgetName\widget\lib\ Or remove the lib folder if you don't include external libraries in the widget.

### AMD caveats
Working with jQuery can be difficult due to the fact that jquery does not adhere to the AMD standard correctly. Check out [Pull Request #13](https://github.com/mendix/AppStoreWidgetBoilerplate/pull/13) or the [Dojo AMD documentation](http://dojotoolkit.org/documentation/tutorials/1.10/modules/index.html) for details.

## Migrating a widget to Dojo AMD

A widget that uses Dojo AMD may not refer to functions like *dojo.forEach* etc. 
All necessary modules must be declared on the module list at the top of the source.

Replacing all 'old' Dojo calls in an existing source can be a bit of a pain.

Here is a list of commonly used functions and their new counterpart:

Old | New
---------- |---------- 
mxui.dom              | domMx
dojo.byId             | dom.byId
dojo.query            | document.querySelector
dojo.forEach          | dojoArray.forEach
dojo.hitch            | lang.hitch
dojo.addClass         | domClass.add
dojo.removeClass      | domClass.remove
dojo.hasClass         | domClass.contains
dojo.replaceClass     | domClass.replace
dojo.empty            | domConstruct.empty
dojo.place            | domConstruct.place 
dojo.on               | on
dojo.window           | win
  
The referenced modules are in the module list of the boilerplate JavaScript.


# Native Bootstrap Carousel

This widget gives you all you need to create a carousel of Bootstrap style using Native JavaScript without jQuery. 

[Bootstrap Example](http://thednp.github.io/bootstrap.native/)
/Components/Carousel

Typical usage
----

This widget gives the user the ability to Display a data of carousel objects with their attached background image. 

 
Features
---
 
- Autoscroll functionality.
- Automatic looping of items.
- Pause the carousel transition on mouse hover and touchdown. 
- Ability to navigate the carousel with left and right keyboard arrows. 
- Ability to set speed of the automatic slide interval (default value 5000 ms).
- Ability to fade effect between the items.
- Responsive & setting with default bootstrap carousel CSS.


Limitations
---

- For correct operation, the image must be attached to each element and have the same size.
 

Installation 
---

- Download the widget from the Mendix App store.
- Move the widget into a data container, for example Data View. 
- Create the entity as CarouselItem data object with attributes Title/Description.
- Create the entity as CarouselItemImage data object with Generalization System.Image.
- Create the Association as CarouselItem_CarouselItemImage [1-1].
- Create a Microflow that will return the list of Carousel data objects.
- Configure the widget within the widget options. 

Configuration
---

![options](http://i.imgur.com/n2occmw.png)


- Datasource Object - The entity CarouselItem.
- Datasource Microflow - The microflow will return the list of Carousel data objects.
- Title - The entity CarouselItem title attribute (optional).
- Description - The entity CarouselItem description attribute (optional).
- Show Controls - The toggle to show / hide the next / previous carousel item controls (arrows).
- Show Dots - The toggle to show / hide the icons of indicates which carousel item is currently shown.
- Auto Scroll - The toggle to enable / disable autoscroll functionality.
- Scroll Speed - Set the speed of the automatic slide interval (milliseconds). 
- Fade Effect - The toggle to enable / disable fade effect between the items. 
- Carousel Id - Set the unique value of ID, if you use more then one carousel on the page.
- Carousel Class - Set the class attribuite for CSS customization (optional). 
- Title Class - Set the class attribuite for CSS customization (optional). 
- Description Class - Set the class attribuite for CSS customization (optional). 
