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

![](images\blue_box_static.png)







