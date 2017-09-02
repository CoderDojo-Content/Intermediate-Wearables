1. Gather all your NeoPixels and some chalk or a pencil. Lay a t-shirt \(or whatever piece of fabric you're making the project on\) out on a flat surface. Arrange the pixels into a shape that you like. I'm going to do a smiley face! Some other ideas are
 * A straight line
 * A heart (eight NeoPixels is perfect for this)
 * Pretend "buttons" down the front of a t-shirt

3. Trace around the outside and the inside of the shape with the pencil or chalk, marking the spot where each NeoPixel is.

4. Decide roughly where you plan to have the Flora and choose one NeoPixel for it to be connected to: this will be the first one you start sewing on. The rest will be connected to each other one by one in a chain.
 
5. Look closely at the NeoPixels. Do you see the little arrows?
 Starting with the first, \(the one you just picked out\), turn each NeoPixel so that its arrows point to the next one in the chain. You should be able to trace out one continuous line along the arrows from the first NeoPixel to the last.
 * The aim is to trace out the line in such a way that it does not cross over itself \(this would cause problems with a short circuit!\)
 
6. Ready to start sewing? Once you have everything marked out, set aside all the pieces and grab a needle and some conductive thread. About 20cm should be enough to begin with if your pixels are quite close together.
 * If you have an embroidery hoop, place your fabric into it. The whole shape you marked out should fit inside.

7. You will sew the **data** line first. Take your first pixel and put it in place, with the arrows pointing towards where the next one will be. Attach it to the fabric by sewing through the pin with the arrow that points **away** from the LED in the centre. This is the **data out** pin. 
 * Be sure to make a secure connection by sewing three or four stitches tightly through the pin.
 
8. Sew a running stitch to the spot where the next pixel will go. Then take the next pixel and place it onto its spot, with the arrows pointing away from the first one and towards the next spot. 

9. Attach it by sewing through the **data in** pin \(remember, this is the pin with the arrow pointing **in towards** the LED in the centre/). Secure the thread with a few stitches at the back of the fabric and cut it short.
 * It is recommended to coat the ends of the thread with clear nail polish after cutting, to prevent fraying and avoid stray threads from causing a short circuit.
 
10. Using a _new piece of conductive thread_, connect the **data out** pin of the second pixel to the **data in** pin of the third pixel. Continue in this way until all the pixels are chained together along their **data** pins, with a separate piece of thread running in between each pair.
 * The chain ends with the last pixel: you don't attach anything to its **data out** pin!
 
11. Next you will connect up all the **negative** pins in the chain, this time using one long piece of conductive thread, about 50-100cm. Sew a few tight stitches through the **-** pin of each pixel starting with the first one and ending with the last. As usual sew with a running stitch in between pixels. 
 * Make sure the thread does not touch or cross any of the thread in the **data** line!

12. With one more long piece of conductive thread, connect all the **+** pins of the pixels in the same way you just connected the **-** pins.

13. Finally, place the Flora on the t-shirt \(make sure it is **not plugged in**!\). You will connect it with running stitches all the way to that first pixel. Using three separate pieces of conductive thread, connect the following pins. Make sure none of the threads touch each other. You can stitch some of the unused pins to the t-shirt with some plain thread to keep the Flora more securely in place.
 * the **#6** pin connects to the **data in** pin of the first NeoPixel
 * the **GND** pin connects to the **-** pin 
 * the **VBATT** pin connects to the **+** pin


 14. It's the moment of truth... plug in your Flora! 
  * If your pixels didn't all light up, don't panic. Some causes could be 
  * A short circuit: are any of the threads touching? Is there anything metallic on the fabric or touching the circuit? Is the fabric wet?
  * Loose connections: The stitches at every pin should be good and tight for a secure connection
  * Correct code uploaded: Does your code have the right number of pixels defined? Did it compile and upload without errors?
 

