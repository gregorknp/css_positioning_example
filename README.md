# css_positioning_example
Example to show how positioning works in CSS

Exercise included in Section 7. Intermediate CSS of "The Complete 2023 Web Development Bootcamp" course.

Given the following html file:

```html
<!DOCTYPE html>
<html>

<head>
  <title>CSS Positioning Exercise</title>
  <style>

  </style>
</head>

<body>
  <div class="blue-box">
    <div class="red-circle">
    </div>
  </div>

</body>

</html>
```

and being only allowed to add code inside the <style> tag, the goal is to create a blue rectangle and a red circle and position them as follows:

![](images/goal.png)

First of all, I'm going to add the blue rectangle. In the html file there is already a div container tagged as "blue-box" class so we only have to use the right properties. Let's try to provide different values to the *position* property and see the effect on the rendered html. 

**position: static**

This is the default positioning style in html so there is no need to specify the position property. We also provide the rest of the properties to match the color and size desired. So, styling the blue-box div as follows:

```html
  <style>
    .blue-box {
      width: 500px;               /* width of 500 pixels */          
      height: 300px;              /* height of 300 pixels */
      background-color: blue;   /* blue as background color */
      left: 200px;                /* element pushed 200 pixels from the left */
      top: 200px;                 /* element pushed 200 pixels from the top */
    }
  </style>
```

it gets rendered as follows:

![](images/blue_box_static.png)

With static positioning, the element is placed just at the bottom of whatever previous element. In this case, as blue-box is the first element in the html file it gets positioned at the top left corner of the browser. Note that with static positioning, the properties left and top don't get applied (both appear greyed out in the inspector).

**position: relative**

With relative positioning the position of the element is relative to its default position. So the element is first placed on its default position and then pushed from the top and pushed from the left using the **top** and **left** properties:

```html
  <style>
    .blue-box {
      width: 500px;               /* width of 500 pixels */          
      height: 300px;              /* height of 300 pixels */
      background-color: blue;   /* blue as background color */
      position: relative;         /* Element positioned relatively to its default position */
      left: 200px;                /* element pushed 200 pixels from the left */
      top: 200px;                 /* element pushed 200 pixels from the top */
    }
  </style>
```

![](images/blue_box_relative.png)

**position: absolute**

absolute positioning places the element relative to the nearest ancestor with a position property set or relative to the top left corner of the webpage.

In this case, as blue-box is the first element in the html file, it has no ancestors so it gets positioned relative to the top left corner of the browser having the same effect as using relative positioning:

```html
  <style>
    .blue-box {
      width: 500px;               /* width of 500 pixels */          
      height: 300px;              /* height of 300 pixels */
      background-color: blue;   /* blue as background color */
      position: absolute;         /* absolute positioning */
      left: 200px;                /* element pushed 200 pixels from the left */
      top: 200px;                 /* element pushed 200 pixels from the top */
    }
  </style>
```

![](images/blue_box_absolute.png)

**position: fixed**

Finally, we have fixed positioning. What this does is to place the element relative to the top left corner of the window and even if we scroll up and down, the element remains in the same position. If the element is the first one in the html file it behaves as if using absolute positioning except for the scrolling:

```html
  <style>
    .blue-box {
      width: 500px;               /* width of 500 pixels */          
      height: 300px;              /* height of 300 pixels */
      background-color: blue;   /* blue as background color */
      position: fixed;            /* fixed positioning */
      left: 200px;                /* element pushed 200 pixels from the left */
      top: 200px;                 /* element pushed 200 pixels from the top */
    }
  </style>
```

![](images/blue_box_fixed.png)





