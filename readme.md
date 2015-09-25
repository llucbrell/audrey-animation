# audrey-animation

> Scion for [audrey-two](https://www.npmjs.com/package/audrey-two) VCCLI (View-Control-Command-Line-Interface) ^v2.0.0

![](https://raw.githubusercontent.com/llucbrell/audrey-animation/master/captura.gif) 

## What this scion does?

Include animation into your audrey-two-view.

## Specifications

Audrey-two version 2.0.0 change the way of control your CLI-views. The tags, now replaced by custom audrey-seeds that you can include or not in your projects.

## Install

Example
```
$ npm install --save audrey-two
  npm install --save audrey-animation
```
## Usage

Example

```js
/* frames is an array with string of every frame
 * remember to format correctly each frame
 */
var myTerminalDisplay={
	body:["x?animation"], //tell audrey where you want to display it
	animation:{
		frames: [
 "     (__)          \n"       
+"     (@@)_____     \n"       
+"     (OO)    /|\\  \n"     
+"       | |--/ | *  \n"         
+"       w w w  w    \n",   

 "    (__)           \n"       
+"    (@@)_____      \n"       
+"    (OO)    /|\\   \n"     
+"      | |--/ | *   \n"         
+"      w w w  w     \n", 

 "   (__)           \n"       
+"   (@@)_____      \n"       
+"   (OO)    /|\\   \n"     
+"     | |--/ | *   \n"         
+"     w w w  w     \n", 

 "  (__)           \n"       
+"  (@@)_____      \n"       
+"  (OO)    /|\\   \n"     
+"    | |--/ | *   \n"         
+"    w w w  w     \n", 

 " (__)           \n"       
+" (@@)_____      \n"       
+" (OO)    /|\\   \n"     
+"   | |--/ | *   \n"         
+"   w w w  w     \n", 

 " (__)           \n"
+" (@@)           \n"
+" (oo)____       \n"
+" /  \\    )\\   \n"
+" \\  /  e_\\ *  \n"
+"  ww            \n",


 " (__)            \n"  
+" (@@)            \n"  
+" (OO)\\          \n"  
+"  /   \\         \n"    
+" w  £__)         \n"
+"                 \n",

 " (__)            \n"  
+" (@~)            \n"  
+" (OO)\\          \n"  
+"  /   \\         \n"    
+" w  £__)         \n"
+"                 \n",

 " (__)          *    *  \n"  
+" (@~)       *     *    \n"  
+" (OO)\\        *    *  \n"  
+"  /   \\           *   \n"    
+" w  £__)      *   *    \n"
+"                 *   * \n",

 " (__)     *  *\n"  
+" (@@)         *\n"  
+" (OO)\\  *  * \n"  
+"  /   \\   ** \n"    
+" w  £__)  *   \n"
+"            * \n",

 " (__)           *\n"  
+" (??)        *   \n"  
+" (OO)\\        * \n"  
+"  /   \\     *   \n"    
+" w  £__)       * \n"
+"             *   \n",

 " (__)       *   \n"  
+" (??)        *  \n"  
+" (OO)\\     *   \n"  
+"  /   \\       *\n"    
+" w  £__)    *   \n"
+"                \n",


  " (__)       *      .----. .----..----..----.   .-.   .-..----.\n"
 +" (xx)        *     | {}  }| {_  | {_  | {_     |  `.'  || {_  \n"
 +" (OO)\\     *       | {}  }| {__ | {__ | |      | |\\ /| || {__\n"
 +"  /   \\       *    `----' `----'`----'`-'      `-' ` `-'`----'\n"
 +" w  £__)    *                                                  \n"
 +"                *                                              \n",
     
        
		], 
		delay: 50, //the time audrey wait untill start the animation
		speed: 250 //the speed of movement between each frame
	} 
};

var audrey2= require('audrey-two');//inicialize audrey
var audrey= audrey2('nameOfView', myTerminalDisplay);

//run your command and pass error objects to audrey

audrey.seed(["audrey-animation-x?"]); //It's an scion don't forget th "x"
//tell audrey that there is a new seed
audrey.encore();
//run audrey
```

## Caveat

As this scion clear several times the screen, the better option to place it is on the header, as the first element. Every object-view before this scion will be removed from the screen.

## Dependencies

Audrey-two make use of...
  
* [cli-frames](https://www.npmjs.com/package/cli-frames) module for the color display.

People and plants really appreciate your great code!
