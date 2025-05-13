# cs16-385-assignment-0---the-image-processing-pipeline-solved
**TO GET THIS SOLUTION VISIT:** [CS16-385 Assignment 0 – The Image Processing Pipeline Solved](https://www.ankitcodinghub.com/product/cs16-385-assignment-0-the-image-processing-pipeline-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94228&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS16-385 Assignment 0 - The Image Processing Pipeline Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Assignment 0

The Image Processing Pipeline

The purpose of this assignment is to introduce you to Matlab as a tool for manipulating images. For this, you will build your own version of a very basic image processing pipeline. As we will see later in the class, the image processing pipeline is the sequence of steps that happens inside a camera, in order to convert a RAW image (roughly speaking, the values measured by the camera sensor) into a regular 8-bit image that you can display on a computer monitor or print on paper. There is a “Hints and Information” section at the end of this document that is likely to help. Uniquely to this assignment, we also provide a solution in the ./solution directory of the homework ZIP archive—but you should really, really, really first try to solve the assignment on your own, before looking at the solution.

Throughout this problem, you will use the file banana slug.tiff included in the ./data directory of the homework ZIP archive. This is a RAW image that was captured with a Canon EOS T3 Rebel camera. We did some very slight pre-processing to the original RAW file, in order to convert it to .tiff format. At the end of this assignment, the image should look something like what is shown in Figure 1. The exact result can vary greatly, depending on the choices you make in your implementation.

Figure 1: One possible rendition of the RAW image provided with the assignment.

Initials. Load the image into Matlab. Originally, it will be in the form of a 2D-array of unsigned integers. Check and report how many bits per integer the image has, and what its width and height is. Then, convert the image into a double-precision array. (See help for functions imread, size, class and double.)

Linearization. The resulting 2D-array is not a linear function with respect to the true “energy” each pixel receives. It is possible that it has an offset due to dark noise (intensity values produced even if no light reaches the pixel), and saturated pixels due to overexposure. Additionally, even though the original data- type of the image was 16 bits, only 14 of those have meaningful information, meaning that the maximum possible value for pixels is 16383 (that’s 214). For the provided image file, you can assume the following: All pixels with a value lower than 2047 correspond to pixels that would be black, were it not for dark noise. All pixels with a value above 15000 are over-exposed pixels. (The values 2047 for the black level and 15000 for saturation are taken from the camera manufacturer).

Convert the image into a linear array within the range [0,1]. Do this by applying a linear transform (shift and scale) to the image, so that the value 2047 is mapped to 0, and the vallue 15000 is mapped to 1. Then, clip negative values to 0, and values greater than 1 to 1. (See help for functions min and max.)

Identifying the correct Bayer pattern. Most cameras do not capture true RGB images. Instead, they use a process called mosaicing, where each pixel captures only one of the three color channels. The most common spatial arrangement of pixels in terms of what color channel they capture is called the Bayer pattern,

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
which says that in each 2 × 2 neighborhood of pixels, 2 pixels capture green, 1 pixel captures red, and 1 pixel captures blue measurements (see Figure 2). The same is true for the camera used to capture our RAW image: If you zoom into the image, you will see the 2 × 2 patches corresponding to the Bayer pattern.

</div>
</div>
<div class="layoutArea">
<div class="column">
Figure 2: The Bayer pattern.

However, we do not know how the Bayer pattern is positioned relative to our image: If you look at the

top-left 2 × 2 image square, it can correspond to any of the four red-green-blue patterns shown in Figure 3.

Figure 3: From left to right: ’grbg’, ’rggb’, ’bggr’, ’gbrg’.

Think of a way for identifying which version of the Bayer patterns applies to our image file, and report

which version you identified. (See Hints and Information.)

White balancing. Before converting the mosaiced image into a proper RGB images, cameras first apply a step called white balancing. Roughly speaking, this involves changing the relative weights of the red, green, and blue measurements, to make sure that materials that are normally white also appear white in the image.

Figure 4: White balancing using the gray world assumption (left) and the white world assumption (right).

Two of the most common algorithms for white balancing use the so-called gray world and white world assumptions, and correspond to the transformations show in Figure 4. Implement both gray world and white world white balancing. At the end of the assignment, check what the image looks like under both white balancing algorithms, and decide which one you like best. (See help for function mean.)

Demosaicing. After white balancing, you want to demosaic the image. This means that you want to convert the partial red, green, and blue color channels you have available because of mosaicing, into three full-resolution color channels. Use bilinear interpolation for demosaicking, as shown in Figure 5. Do not implement bilinear interpolation manually! Instead, read the documentation to learn how to use Matlab’s interp2 function for this purpose.

Brightness adjustment and gamma correction (20 points). You now have a 16-bit, full-resolution, linear RGB image. Because of the scaling you did at the start of the assignment, the image pixel values may not be in a range appropriate for display. As a result, when displaying the image, it will appear very dark.

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Figure 5: Demosaicing is the process of turning “filling-in” gaps in the three color channels, to obtain a full-resolution RGB image. This can be done by performing bilinear interpolation in each of the partial color channels measured by the sensor.

Brighten the image by linearly scaling it by some number. Select the scale as a percentage of the pre- brightening maximum grayscale value. (See help for rgb2gray for converting the image to grayscale). The correct percentage is highly subjective, so you should experiment with many different percentages and report and use what percentage looks best to you.

Before having an image that can be properly displayed, the last step you need to do is tone reproduction, also known as gamma correction. This is a non-linear transformation of intensity values, which roughly speaking is used to better match sensor measurements to the response function of common displays. For this, implement the following non-linear transform, then apply it to the image:

</div>
</div>
<div class="layoutArea">
<div class="column">
􏰍 12.92 · Clinear, Cnon-linear = 1

</div>
<div class="column">
− 0.055,

</div>
<div class="column">
Clinear ≤ 0.0031308 Clinear ≥ 0.0031308

</div>
<div class="column">
(1)

</div>
</div>
<div class="layoutArea">
<div class="column">
(1 + 0.055) · C 2.4 linear

</div>
</div>
<div class="layoutArea">
<div class="column">
where C = {R,G,B} is each of the red, green, and blue channels. This function may look completely arbitrary, but it comes from the sRGB standard. It is a good default choice if the camera’s true gamma correction curve is not known. We will discuss sRGB in class, but you are welcome to read up on Wikipedia.

Compression. Finally, it is time to store the image, either with or without compression. Use the imwrite command to store the image in .PNG format (no compression), and also in .JPEG format with quality setting 95. This setting determines the amount of compression. Can you tell the difference between the two files? The compression ratio is the ratio between the size of the uncompressed file (in bytes) and the size of the compressed file (in bytes). What is the compression ratio?

By changing the JPEG quality settings, determine the lowest setting for which the compressed image is indistinguishable from the original. What is the compression ratio?

Hints and Information

• To get help on a particular function in Matlab, type help &lt;function&gt;. To get a list of functions related to a particular keyword, use the lookfor function. We will be making extensive use of the Image Processing Toolbox, and a list of the functions in that toolbox is generated by typing help images. Print your results (to a printer or to a file) using the print command, and when making hardcopies please save space by using subplot whenever possible. As an example, the following Matlab script loads three images, displays them in a figure and prints the figure to a PNG file.

<pre>           % read three images from current directory
           im1 = imread(‘image1.tiff’);
           im2 = imread(‘image2.tiff’);
           im3 = imread(‘image3.tiff’);
</pre>
<pre>           % display images in a figure, side-by-side
           figure;           % create a new figure
           imshow(im1);      % display an image
           title(‘Image 1’); % add a title
</pre>
<pre>           % print the displayed figure a PNG file. You can also print from the figure menubar.
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
<pre>           print -dpng output.png
</pre>
• You will find it very helpful to display intermediate results while you are implementing the image processing pipeline. However, before you apply the brightening and gamma correction, you will find that displayed images will look completely black. To be able to see something more meaningful, you can use the following command to display an intermediate image im intermediate.

<pre>           figure; imshow(min(1, im_intermediate * 5));
</pre>
For example, Figure 6 shows what you should see using this command after the linearization step.

Figure 6: Left: The linear RAW image (brightness increased by 5). Right: Crop showing the Bayer pattern.

• The colon operator : allows to form arrays out of subsets of other arrays. In the following example, given an original image im, it creates three other images, each with only one-fourth the pixels of the originals. The pixels of each of the corresponding sub-images are shown in Figure . You can also use the function cat to combine these three images into a single 3-channel RGB image.

</div>
</div>
<div class="layoutArea">
<div class="column">
Credit

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>% create three sub-images of im as shown in figure below
im1 = im(1:2:end, 1:2:end)
im2 = im(1:2:end, 2:2:end);
im3 = im(2:2:end, 1:2:end);
</pre>
<pre>% combine the above images into an RGB image, such that im1 is the red,
% im2 is the green, and im3 is the blue channel
im_rgb = cat(3, im1, im2, im3);
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
The RAW image used in this assignment, and some inspiration for the questions, came from Robert Sumner’s popular guide for reading and processing RAW files.

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
