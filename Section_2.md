How to create an SVG within HTML

This is the utmost basic code for inserting a filled-in rectangle using html. (Note: I use {} instead of <> for visualization purposes)

{html}

 {svg width="100" height="50"}
 
  {rect width="100" height="50" fill="blue" /}
  
 {/svg}
 
{/html}

This produces a container with the width of 100 units and a height of 50 units. This is required everytime to set the parameters of your container. 

The rectangle is self explanatory. The {rect} "element" serves as a built in function that only need width and height to be specified. If the fill parameter is not entered, then it would produce a transparently outlined rectangle. 

If you wanted to to create a rectangle that was not filled but had an outline you can use the stroke paramter.

{rect width="100" height="50" stroke="black" /}

There are more ways to expand and enhance the triangle beyond fill and stroke.

Now onto a more complicated tutorial that utilizes multiple elements. This is how to combine elements to make a church:

{svg width="200" height="200"}
  {!-- Church Building --}
  {rect x="50" y="50" width="100" height="100" fill="tan" /}

  {!-- Roof (triangle/polygon) --}
  {polygon points="50,50 100,10 150,50" fill="brown" /}

  {!-- Cross --}
  {rect x="95" y="35" width="10" height="50" fill="gray" /}
  {rect x="85" y="45" width="30" height="10" fill="gray" /}

  {!-- Door --}
  {rect x="80" y="100" width="40" height="50" fill="brown" /}

  {!-- Windows --}
  {rect x="60" y="60" width="20" height="20" fill="yellow" /}
  {rect x="120" y="60" width="20" height="20" fill="yellow" /}
{/svg}

A lot to unpack here:

The new element used: polygon
The {polygon} element defines a closed shape consisting of a set of connected straight line segments. The last point is connected to the first point.

For the roof I created a triangle by specifying 3 different vertices within the svg container.


