# javascript-enemy-movements-three

Just like the previous movement types, copy and paste the code from the previous movement(two in this case) to start editting to the next movement type for coherency
Change the source image to three and the spriteWidth and height to match the image's sprite
Comment x and y in update to prevent sprite from moving
To cycle horizontal movement within a certain range, just like movement two which cycled on the vertical movement using y, use Math.sin method on x in update
Assign x in update to Math.sin(this.angle \* Math.PI/180) to line them up vertically
Multiplying the value of Math.sin by let's say a 100 will show a horizontal movement
angleSpeed controls how fast the angle is moving so changing the range of angleSpeed in the constructor will change the speed
Replace 0.2 of angleSpeed in constructor to 2 to increase the movement speed
To move the sprite to the right, add a positive number after the calculation of number \* Math.sin... to push them to the right
To center the sprites horizontally so that they do not disappear outside of the canvas, remove the hardcoded positive number and add the length of the canvas divided by 2 offsetted by Enemy's class width divided by 2
To randomise the horizontal movement, change the range of curve in constructor from 0 to 200 and replace the hardcoded 100 of x in update to this.curve
Math.sin() will return a value between -1 and 1
Since we change the range of curve from 0 to 200, when multiplied against Math.sin it will return a value between -200 to 200 now
Since angle is every increasing with the increment operator, Math.sin will now bounce endlessly between -1 and 1 multiplied by 200 which results in the values between -200 to 200 instead
Uncomment y in update and copy paste the calculation of x into y
Change canvas.width and this.width to height instead
Also, change Math.sin to Math.cos
Math.sin (as seen in movement type two) does calculations for vertical movements whereas Math.cos is its opposite and does it for vertical movements
Math.sin is the relationship between the hypotenuse and opposite side of a given angle
Math.cos is the relationship between the hypotenuse and adjacent side of a given angle
By combining the 2, you will achive a circular motion in the animation
Currently, this.curve determines the radius of the motion randomised from 0 to 200
For now, give it a range from 50 to 250
This will increase the min and max circular motion
You can increase the speed of the motion in angleSpeed the same way by increasing the min and max
Math.sin and Math.cos is currently the same so the circular motion is regular
To make it irregular, you can change the value of the hardcoded 180 in x and y where the ratio would determine the number of cycles of horizontal and vertical movement (i.e 2:1 ratio 360 to 180 will result in x having 2 cycles when y has 1 cycle)
Uneven ratios will result in more chaotic movements
Lower values will make the motion faster while higher values slows down the motion
Play with numbers in angleSpeed, xy hardcoded value variables, interchanging Math.sin and Math.cos in xy to learn the behavior or simply change the motion of your sprites
Currently, you are not using the full canvas space as you are using a set curve property with a set range
Replace this.curve of xy in update with canvas.width and height respectively, dividing each of them by 2 to cover width of canvas instead of the radius
Now the movement of the sprites are more distinct since the whole canvas is used
angle in constructor determines the starting point of the sprite along the path it is taking
You can randomise it by using Math.random method and set a range
Movement type three done! (kinda)
