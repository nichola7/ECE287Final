# ECE287Final
Scott Nicholson
Storm Nicholson

A game we made in verilog for the final project for ECE287

A presentation of this project/game can be found here. Youtube demo: https://www.youtube.com/watch?v=gUmKXUYoEVI

Reports can be pretty boring. So I decided to spice it up a little.

A short time ago in an EE lab not too far away...

It is a period of civil war. Two partners, who weren't originally supposed to work together, must overcome varying work schedules and idealogical differences to come together to win their first victory in ECE 287. During the battle the partners decided (to the disdain of one of the partners, though at the end he was thrilled with the final product) to try and use a DE2-115 board to implement a VGA and make a space invaders type of game. Space invaders in a game where a user controlled ship shoots at enemies and destroys them and the object of the game is to destroy all of the ships to win. Our game must be implemented using verilog with the DE2-115. This implementation requires displaying a blue playing surface (the color could be changed in the verilog code) on a monitor with different colored rectangles. This rectangles(whose color could also be changed in the verilog code) represent enemy ships(in red) and the player ship(in chartruese, which is case you don't know is a yellowish color). Basically to paint on the screen, the verilog program goes through each pixel from, left to right and up to down, and decides what color to paint it. The program basically calls for a continuous painting of the screen so when an action occurs(like a ship being destroyed) the program paints those pixels the color they should be. In the case of a ship being destroyed, the program moves the ship off screen into the porch and since the ship is no longer on screen, the code paints it the correct color. The continous checking of pixels occurs with the clock implmented which very quickly cycles through actions. The rectangles are painted on the screen when the game is first sent from the board to the monitor. The verilog code specifies which area of pixels to be colored, and what color is to be used. The color is determined with the RGB values, each individual value are implemented as an output register. A button on the DE2-115 board shoots a green lazer from the player ship and sends it towards the enemy ship. When the green lazer comes in contact with the red rectangles the enemy ship "get destroyed" and disappear. When all the ships have disappeared you win the game and a yellow smily face appears. Another button will reset the rectangles and restart the game. In conclusion, we sought to create a space invaders type game with the DE2-115 board. Using verilog we implemented a VGA so the game would display to a monitor and the game functions as intended. 

Code to get the VGA working, the hv_sync.v file, was from classmate Logan Johnson, and the counter in the other file, finalScottStorm.v, was also from Logan. 
