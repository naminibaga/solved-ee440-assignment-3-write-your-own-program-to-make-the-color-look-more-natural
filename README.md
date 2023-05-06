Download Link: https://assignmentchef.com/product/solved-ee440-assignment-3-write-your-own-program-to-make-the-color-look-more-natural
<br>
<ol>

 <li>The color of <strong>bmp</strong> does not look right. Please write your own program to make the color look more natural. You could try different methods to make it look better. Explain the final method you use and how it works.</li>

</ol>




<strong><em>Hint</em></strong>: For example, you might think there is one color that seems overwhelming, or maybe some colors are not strong enough. You can play with the colors to figure out how to make the image look better….




an image which the color does not look right                                   a more natural image




<ol start="2">

 <li>You have two low-quality images (<strong>jpg, 3_3.jpg</strong>) that you want to enhance. You will exam the following three general histogram-based enhancement algorithms:</li>

</ol>




<ol>

 <li>Linear stretching;</li>

</ol>

<em>One simple way to do linear stretching is, for example, if majority of original image’s brightness (V channel in HSV or I channel is HSI) values fall into range X to Y, we could define a linear function that map from X—Y to 0—255. <strong>Note:</strong> Linear stretching may not work well for some images if their original dynamic range is already in 0-255.</em> b. Histogram equalization;

<ol>

 <li>Histogram specification.</li>

</ol>




For each image and each method, please submit the original and the new image after processing. For the original and new images, please also include their histogram and cdf plots for you to get a better understanding of what’s going on with these processing in regard with the image histogram. Compare the effects of these methods. For each image, please comment on the effects and pick up the best method for that image in your opinion. <strong>(70</strong> <strong>points)</strong>

<strong>       </strong>

<strong><em>Hints</em></strong>:




<ol>

 <li>You need to implement your own functions for linear stretching, histogram equalization, and specification. You may find these commands helpful: <em>rgb2hsv</em>, <em>hsv2rgb, subplot, imshow, cumsum, imhist.</em></li>

</ol>




<ol start="2">

 <li>You may want to convert the image to HSV first before taking any operations; specifically, you want to process the V channel (value, i.e., intensity) only. After the V channel is altered, you want to combine it with the original H and S channels and convert it back to RGB.</li>

</ol>




<ol start="3">

 <li>For histogram equalization, compute pdf and cdf first and then use the cdf as the transform function. You can use command <em>imhist</em> to help you get the image histogram and then use command <em>cumsum</em> to get the cdf from histogram, but please DON’T use command <em>histeq</em> to directly perform histogram equalization.</li>

</ol>




<ol start="4">

 <li>For histogram specification, you may specify any histogram to get the best result. Note that if you specify the target histogram as a uniform distribution, you’re doing histogram equalization. You can also try a normal distribution as the specified histogram to get the transform function and see how the result turns out. Use command <em>normpdf</em> to generate a normally distributed sequence in MATLAB. Use command <em>help normpdf</em> to see how to use this function to generate a desired normally distributed histogram. Remember this histogram has 256 bins.</li>

</ol>