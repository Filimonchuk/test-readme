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

![entity](https://github.com/Filimonchuk/test-readme/blob/master/assets/entity_create.png)

- Create a Microflow that will return the list of Carousel data objects.

![mf](https://github.com/Filimonchuk/test-readme/blob/master/assets/mf_create.png)

- Configure the widget within the widget options. 

Configuration
---

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
