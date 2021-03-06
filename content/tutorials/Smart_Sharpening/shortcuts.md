Title: "Smart" Sharpening Shortcuts
Date: 2004
Modified: 2015-10-05T11:26:57-05:00
Author: Eric R. Jeschke

<p>
  Text and images Copyright (C) 2002 <a href="mail:People-Jeschke_Eric_R">Eric R. Jeschke</a> and may not be used without permission of the author.
</p>

<h2>Intention</h2>
<p>
  Maybe you think the smart sharpening method is too complicated, or too lengthy, 
  or just not worth it for the benefit. There are many variations on this technique, 
  some of which are not as lengthy as the "full" technique, but may still produce better results than a straightforward unsharp mask operation.
</p>

<h2>Possible combinations</h2>
<ol>
  <li>Decompose into LAB, and prepare a sharpening mask. Only the edges in the luminosity channel are sharpened. 
  This is the full procedure described in the tutorial.</li>
  <li>Decompose into HSV, and prepare a sharpening mask. Only the edges in the value channel are sharpened. 
  A variation on the full procedure described in the tutorial.</li>
  <li>Don't decompose into LAB, but do prepare a sharpening mask. Only the edges in all RGB channels are sharpened. 
  A good method if losing information due to mode changes is a concern.</li>
  <li>Don't decompose into LAB, but do prepare a sharpening mask. Only the edges in the red channel are sharpened.
  <br /><br />
  The red channel is used since it usually contains most of the luminosity information for the image. 
  Once you have the sharpening mask created as described earlier 
  and have converted it into a selection, go to the Layers dialog, click on the Channels tab and unselect the Green and Blue channels. Now apply the filter.</li>
  <li>Don't decompose into LAB, and don't prepare a sharpening mask. The entire image is sharpened, but only in the red channel. 
  We can't use as large an amount of sharpening, or it will exacerbate the noise.</li>
  <li>Decompose into LAB, but don't prepare a sharpening mask. The entire image is sharpened, but only in the luminosity channel. 
  We can't use as large an amount of sharpening, or it will exacerbate the noise.</li>
  <li>Decompose into HSV, but don't prepare a sharpening mask. The entire image is sharpened, but only in the value channel. 
  We can't use as large an amount of sharpening, or it will exacerbate the noise.</li>
  <li>Sharpen the entire image, all RGB channels.</li>
</ol>

<h2>Results</h2>
<p>
  Compare for yourself!
  <br />
  Here are the results for the combinations listed above. Look for the sharpness in the eye lines, 
  and CCD noise in the shadows of the face and in the door frame of the car.
</p>

<p class="images">
  <img src="{filename}image-luminosityedgesharpened-zoomed100.jpg" alt="image-luminosityedgesharpened-zoomed100.jpg" />
</p>
<p>
  1. Sharpening mask (edges only), luminosity channel only (LAB decompose/compose).
  <br />
  (Radius=1, Amount=2.0, Threshold=0)
</p>

<p class="images">
  <img src="{filename}image-valueedgesharpened-zoomed100.jpg" alt="image-valueedgesharpened-zoomed100.jpg" />
</p>
<p>
  2. Sharpening mask (edges only), value channel only (HSV decompose/compose).
  <br />
  (Radius=1, Amount=2.0, Threshold=0)
</p>

<p class="images">
  <img src="{filename}image-edgesharpened-zoomed100.jpg" alt="image-edgesharpened-zoomed100.jpg" />
</p>
<p>
  3. Sharpening mask (edges only), all RGB channels (no decompose/compose). First of the "shortcuts".
  <br />
  (Radius=1, Amount=2.0, Threshold=0)
  <br />
  This does nearly as good a job as the "full" smart sharpening technique. If your image is not particularly noisy, this is the way to go.
</p>

<p class="images">
  <img src="{filename}image-rededgesharpened-zoomed100.jpg" alt="image-rededgesharpened-zoomed100.jpg" />
</p>
<p>
  4. Sharpening mask (edges only), red channel only (no decompose/compose).
  <br />
  (Radius=1, Amount=2.0, Threshold=0)
  <br />
  At first you'd think that this would produce a better result than #3. It's very good as far as not enhancing noise, but it's clearly not as sharp.
</p>

<p class="images">
  <img src="{filename}image-redsharpened-zoomed100.jpg" alt="image-redsharpened-zoomed100.jpg" />
</p>
<p>
  5. No sharpening mask (entire image), red channel only (no decompose/compose).
  <br />
  (Radius=1, Amount=1.0, Threshold=0)
  <br />
  This one is a toss-up with shortcut #6. There is more noise than in shortcuts #3 and #4, but less than in #6. It's also less sharp than #6.
</p>

<p class="images">
  <img src="{filename}image-luminositysharpened-zoomed100.jpg" alt="image-luminositysharpened-zoomed100.jpg" />
</p>
<p>
  6. No sharpening mask (entire image), luminosity channel only (LAB decompose/compose).
  <br />
  (Radius=1, Amount=1.0, Threshold=0)
  <br />
  Sharper than #5, but with more visible noise. Noise is barely, perceptibly less than in #7 &amp; #8.
</p>

<p class="images">
  <img src="{filename}image-valuesharpened-zoomed100.jpg" alt="image-valuesharpened-zoomed100.jpg" />
</p>
<p>
  7. No sharpening mask (entire image), value channel only (HSV decompose/compose).
  <br />
  (Radius=1, Amount=1.0, Threshold=0)
  <br />
  Hardly seems worth the decompose/compose steps, noise is as bad as in #8.
</p>

<p class="images">
  <img src="{filename}image-regularsharpened-zoomed100.jpg" alt="image-regularsharpened-zoomed100.jpg" />
</p>
<p>
  8. No sharpening mask (entire image), all RGB channels (no decompose/compose).
  <br />
  (Radius=1, Amount=1.0, Threshold=0)
  <br />
  This is a regular unsharp mask operation.
</p>

<p class="images">
  <img src="{filename}image-original-zoomed100.jpg" alt="image-original-zoomed100.jpg" />
</p>
<p>
  9. Unsharpened original.
</p>

<p>
  You may also be interested in another shortcut technique: <a href="/tutorials/Smart_Sharpening/warp-sharp.html">the "warp sharp" script</a>.
</p>

<p>
The original tutorial used to appear on gimpguru.org.
</p>
