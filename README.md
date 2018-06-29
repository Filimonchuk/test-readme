# Native Bootstrap Carousel

This widget gives you all you need to create a carousel of Bootstrap style using Native JavaScript without jQuery. 

[http://thednp.github.io/bootstrap.native](http://thednp.github.io/bootstrap.native/)
/Components/Carousel

Typical usage
----

This widget gives the user the ability to display a data of carousel objects with their attached background image. 

 
Features
---
 
- Autoscroll functionality.
- Automatic looping of items.
- Pause the carousel transition on mouse hover and touchdown. 
- Ability to navigate the carousel with left and right keyboard arrows. 
- Ability to set speed of the automatic slide interval.
- Ability to fade effect between the items.
- Responsive & setting with default bootstrap carousel CSS.
- Ability to customization with custom CSS styles.


Limitations
---

- For correct operation, the images must be attached to each item and have the same size.
 

Installation 
---

- Download the widget from the Mendix App store.
- Move the widget into a data container, for example Data View. 
- Create the entity as CarouselItem data object with attributes Title/Description.
- Create the entity as CarouselItemImage data object with Generalization System.Image.
- Create the Association as CarouselItem_CarouselItemImage [1-1].
![entity](../master/assets/entity_create.png)

- Create a Microflow that will return the list of Carousel data objects.
![mf](https://modelshare.mendix.com/models/93c083d9-7cf9-4a83-b018-3bcf332d7a81/microflow-image?embed=true)


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
- Scroll Speed - Set the speed of the automatic slide interval (milliseconds, default value 5000). 
- Fade Effect - The toggle to enable / disable fade effect between the items. 
- Carousel Id - Set the unique value of ID, if you use more then one carousel on the page.
- Carousel Class - Set the class attribuite for CSS customization (optional). 
- Title Class - Set the class attribuite for CSS customization (optional). 
- Description Class - Set the class attribuite for CSS customization (optional). 
