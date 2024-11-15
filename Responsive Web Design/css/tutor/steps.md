## Step 49

You've learned a few ways to set flat colors in CSS, but you can also use a color transition, or gradient, on an element.

A gradient is when one color transitions into another. The CSS linear-gradient function lets you control the direction of the transition along a line, and which colors are used.

One thing to remember is that the linear-gradient function actually **creates an image element**, and is usually paired with the background property which can accept an image as a value.

In the .red CSS rule, change the background-color property to background.


## Step 50

The linear-gradient function is very flexible -- here is the basic syntax you'll use in this tutorial:
Example Code

linear-gradient(gradientDirection, color1, color2, ...);

gradientDirection is the direction of the line used for the transition. color1 and color2 are color arguments, which are the colors that will be used in the transition itself. These can be any type of color, including color keywords, hex, rgb, or hsl.

Now you'll apply a red-to-green gradient along a 90 degree line to the first marker.

First, in the .red CSS rule, set the background property to linear-gradient(), and pass it the value 90deg as the gradientDirection.

## Step 51

You'll use the rgb function for the colors of this gradient.

In the linear-gradient function, use the rgb function to set the first color argument to pure red.

## Step 54

Color-stops allow you to fine-tune where colors are placed along the gradient line. They are a length unit like px or percentages that follow a color in the linear-gradient function.

For example, in this red-black gradient, the transition from red to black takes place at the 90% point along the gradient line, so red takes up most of the available space:
Example Code

linear-gradient(90deg, red 90%, black);

In the linear-gradient function, add a 75% color stop after the first red color argument. Do not add color stops to the other colors arguments.

## Step 55

Now that you know the basics of how the linear-gradient function and color-stops work, you can use them to make the markers look more realistic.

In the linear-gradient function, set gradientDirection to 180deg.

## Step 56

Next, set the color-stop for red to 0%, the color-stop for green to 50%, and the color-stop for blue to 100%.

## Step 57 Passed

Now that the color-stops are set, you'll apply different shades of red to each color argument in the linear-gradient function. The shades on the top and bottom edges of the marker will be darker, while the one in the middle will be lighter, as if there's a light above it.

For the first color argument, which is currently pure red, update the rgb function so the value for red is 122, the value for green is 74, and the value for blue is 14.

## Step 64

Even without the color-stops, you might have noticed that the colors for the green marker transition at the same points as the red marker. The first color is at the start (0%), the second is in the middle (50%), and the last is at the end (100%) of the gradient line.

The linear-gradient function automatically calculates these values for you, and places colors evenly along the gradient line by default.

In the .red CSS rule, remove the three color stops from the linear-gradient function to clean up your code a bit.

## Step 65

If no gradientDirection argument is provided to the linear-gradient function, it arranges colors from top to bottom, or along a 180 degree line, by default.

Clean up your code a little more by removing the gradientDirection argument from both linear-gradient functions.


## Step 75

You're already familiar with using the rgb function to set colors. To add an alpha channel to an rgb color, use the rgba function instead.

The rgba function works just like the rgb function, but takes one more number from 0 to 1.0 for the alpha channel:
Example Code

rgba(redValue, greenValue, blueValue, alphaValue);

You can also use an alpha channel with hsl and hex colors. You will see how to do that soon.

In the .sleeve rule, use the rgba function to set the background-color property to pure white with 50% opacity.

## Step 82

The border-left shorthand property lets you to set the left border's width, style, and color at the same time.

Here is the syntax:
Example Code

border-left: width style color;

In the .sleeve CSS rule, replace the border-left-width, border-left-style, and border-left-color properties with the border-left shorthand property. The values for the width, style, and color of the left border should be the same.

## Step 86

The last thing you'll do is add a slight shadow to each marker to make them look even more realistic.

The box-shadow property lets you apply one or more shadows around an element. Here is basic syntax:
Example Code

box-shadow: offsetX offsetY color;

Here's how the offsetX and offsetY values work:

    both offsetX and offsetY accept number values in px and other CSS units
    a positive offsetX value moves the shadow right and a negative value moves it left
    a positive offsetY value moves the shadow down and a negative value moves it up
    if you want a value of zero (0) for any or both offsetX and offsetY, you don't need to add a unit. Every browser understands that zero means no change.

The height and width of the shadow is determined by the height and width of the element it's applied to. You can also use an optional spreadRadius value to spread out the reach of the shadow. More on that later.

Start by adding a simple shadow to the red marker.

In the .red CSS rule, add the box-shadow property with the values 5px for offsetX, 5px for offsetY, and red for color.


## Step 88

Notice that the edges of the shadow are sharp. This is because there is an optional blurRadius value for the box-shadow property:
Example Code

box-shadow: offsetX offsetY blurRadius color;

If a blurRadius value isn't included, it defaults to 0 and produces sharp edges. The higher the value of blurRadius, the greater the blurring effect is.

In the .green CSS rule, add the box-shadow property with the values 5px for offsetX, 5px for offsetY, 5px for blurRadius, and green for color.

## Step 89

But what if you wanted to expand the shadow out further? You can do that with the optional spreadRadius value:
Example Code

box-shadow: offsetX offsetY blurRadius spreadRadius color;

Like blurRadius, spreadRadius defaults to 0 if it isn't included.

Practice by adding a 5 pixel shadow directly around the blue marker.

In the .blue CSS rule, add the box-shadow property with the values 0 for offsetX, 0 for offsetY, 0 for blurRadius, 5px for spreadRadius, and blue for color.
