Title: "Warp" Sharpening
Date: 2004
Modified: 2015-10-05T11:26:57-05:00
Author: Eric R. Jeschke


<p>
  Text and images Copyright (C) 2002 <a href="mail:People-Jeschke_Eric_R">Eric R. Jeschke</a> and may not be used without permission of the author.
</p>

<h2>Intention</h2>
<p>
  Thanks to Branko Collin for bringing to my attention <a href="http://www.home.unix-ag.org/simon/gimp/warp-sharp.html">Simon Budig's "warp sharp" script</a>. 
  This is a Script-Fu script that you can put in your GIMP folder and run straight from GIMP. 
  This is a very impressive script and a nice tool to have in your GIMP toolbox.
</p>
<p>
  I haven't yet had a chance to experiment with it too much beyond the default settings, 
  but I have tried it on a couple of the images used in my full smart sharpening tutorial. 
  Here are the results:
</p>

<h2>First image</h2>
<p class="images">
  <img src="{filename}example1-original-zoomed100.jpg" alt="example1-original-zoomed100.jpg" />
</p>
<p>
  1. Original image, zoomed 100%.
</p>

<p class="images">
  <img src="{filename}example1-unsharpmask-zoomed100.jpg" alt="example1-unsharpmask-zoomed100.jpg" />
</p>
<p>
  2. Standard unsharp mask filter, all RGB channels.
  <br />
  (Radius=1, Amount=1.0, Threshold=0) Yuk. This is why you want to smart sharpen.
</p>

<p class="images">
  <img src="{filename}example1-warpsharp-zoomed100.jpg" alt="example1-warpsharp-zoomed100.jpg" />
</p>
<p>
  3. Warp sharp script, all RGB channels.
  <br />
  (default parameters: Edge detection=7.0, Blur radius=3.0, Bump depth=2, Displace intensity=2.5)
</p>

<p class="images">
  <img src="{filename}example1-warpsharp-luminosityonly-zoomed100.jpg" alt="example1-warpsharp-luminosityonly-zoomed100.jpg" />
</p>
<p>
  4. Warp sharp script, luminosity channel only.
  <br />
  (default parameters: Edge detection=7.0, Blur radius=3.0, Bump depth=2, Displace intensity=2.5)
</p>
<p>
  I don't see much difference between this and #3. I wouldn't really expect to, since the warp sharp script appears to operate on edges only. 
  I did find that the edges are not as "squeezed" here--they are slightly ragged, 
  more like the other, non-warp sharpening techniques. See the discussion below for more on this.
</p>

<p class="images">
  <img src="{filename}example1-smartsharp-zoomed100.jpg" alt="example1-smartsharp-zoomed100.jpg" />
</p>
<p>
  5. Smart sharpened (edges, luminosity channel only).
  <br />
  The full technique from <a href="/tutorials/Smart_Sharpening/">the tutorial</a>. 
  I think this one still has less noise, or at least the noise is more "smoothed out" and less objectionable than in #4.
</p>

<p class="images">
  <img src="{filename}example1-warpsharp-luminosityonly.jpg" alt="example1-warpsharp-luminosityonly.jpg" />
</p>
<p>
  Warp sharp script, luminosity channel only (same as #4--unzoomed).
  <br />
  Here the difference is more visible and striking. Compare to below.
</p>

<p class="images">
  <img src="{filename}example1-smartsharp.jpg" alt="example1-smartsharp.jpg" />
</p>
<p>
  Smart sharpened (edges, luminosity channel only; same as #5--unzoomed).
  <br />
  To my eye this one is definitely better. Notice the arm, the face and the white wall in the upper left and compare to above.
</p>

<h2>Tutorial image</h2>
<p>
  Here's the main test image from the tutorial:
</p>
<p class="images">
  <img src="{filename}image-compare-original.jpg" alt="image-compare-original.jpg" />
</p>
<p>
  1. Original image.
  <br />
  Examine the seam between the driver's window frame and the rear window frame.
</p>

<p class="images">
  <img src="{filename}image-compare-warpsharp.jpg" alt="image-compare-warpsharp.jpg" />
</p>
<p>
  2. Warp sharpened.
  <br />
  (default parameters: Edge detection=7.0, Blur radius=3.0, Bump depth=2, Displace intensity=2.5) Compare the seam to the above image. Very similar.
</p>

<p class="images">
  <img src="{filename}image-compare-smartsharp.jpg" alt="image-compare-smartsharp.jpg" />
</p>
<p>
  3. Smart sharpened (edges, luminosity channel only).
  <br />
  Note how the seam contrast is exaggerated, along with every nick and cut along the seam.
</p>

<p class="images">
  <img src="{filename}image-compare-warpsharp-zoomed100.jpg" alt="image-compare-warpsharp-zoomed100.jpg" />
</p>
<p>
  Warp sharpened, zoomed to 100%.
  <br />
  Examine the catchlight in the eyes, the edge of the iris, and the edge of the cheek/chin on the left.
</p>

<p class="images">
  <img src="{filename}image-compare-smartsharp-zoomed100.jpg" alt="image-compare-smartsharp-zoomed100.jpg" />
</p>
<p>
  Smart sharpened, zoomed to 100%.
  <br />
  Compare the catchlights and the iris/chin/cheek edges.
</p>

<h2>Discussion</h2>
<p>
  Obviously this is a very preliminary and cursory examination, and further experimentation 
  with the warp sharp script parameters is necessary before making any substantive 
  judgements about the quality of warp sharping. What follows are my first impressions only.
</p>
<p>
  In the noisy image, the smart sharpened image appears noticeably better to my eye 
  than the warp sharpened image, at least viewed on screen and zoomed out. Noise is noticeably less visible.
</p>
<p>
  On the less noisy image the results are not so clear cut. The two things that stand out to me in 
  comparing the warp sharpened version to the smart sharpened version are that
</p>
<ol>
  <li>the warp sharpening appears not to increase the contrast as much (e.g. in the window seam). 
  Since I am not sure what constitutes a comparable "amount" of sharpening in 
  the warp sharpen parameters, the contrast could be simply due to the fact that I cranked 
  the smart sharpened amount parameter up to 2.0, and that this is much greater than 
  the default level of "amount" in the warp sharpen (I did in fact compare with an 
  amount of 1.0 also and found that the contrast was still greater than in the warp sharpened version). 
  In any case, in this image the seam between the windows is more pleasing in the warp sharpened version.
  </li>
  <li>the warp sharpening appears to have a pronounced effect in "squeezing" the edges (as in fact it is advertised to do), which results in less "ragged" edges 
  (e.g. in the cheek/iris edges). I'm not sure what to think about this. My initial reaction is that the edges do not look quite as natural. For example, 
  the iris outline is just not naturally that smooth of an edge. It seems like the sharpening process should increase contrast between edges, 
  but that shrinking the edges is not necessarily a desirable byproduct. However, the zoomed warp sharpened image looks sharper than the zoomed smart 
  sharpened image because of the less ragged edges throughout. Zoomed out it is not as apparent.
  </li>
</ol>

<h2>Conclusion</h2>
<p>
  More experimentation is necessary! For now, I am convinced that the warp sharpen script is a useful addition to the GIMP toolbox. 
  Certainly as a convenience sharpening option it is unmatched: just run the script.
</p>

<h2>Getting the warp-sharp script</h2>
<p>
  Here is a <a href="http://www.home.unix-ag.org/simon/gimp/warp-sharp.html">link to the script authors site</a>. 
  Download the script and put it into your .gimp-2.2/scripts folder. 
  Restart GIMP and you should see warp sharpen as an option off of the "Alchemy" script-fu menu.
</p>

<p>
    The original tutorial used to appear on <a href="https://web.archive.org/web/20140704043127/http://gimpguru.org/tutorials/smartsharpening/warp-sharpening/">gimpguru</a>.
</p>
