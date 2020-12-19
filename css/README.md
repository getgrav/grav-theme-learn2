<!-- This document describes how to format pages for proper styling. -->

!!! At beginning over every page, insert
	<a name="top"></a>
	<hr class="hrfade">

!!! Link to top:
	<p class="top"><a href="#top">Back to Top</a></p>

!!! At beginning of every lesson page, insert:
	<a name="top"></a>
	<!-- To add a link back to the top use <p class="top"><a href="#top">Back to Top</a></p> -->
	<hr class="hrfade">
	<div class="inthislesson">
		<div class="innerborder">
		<h1>in this lesson</h1>
		<!-- keep above title all lower case -->
		<p>quick intro sentence or two</p>
		<ul>
			<li><a href="#anchorname"> name of first h2</a></li>
			<li><a href="#anchorname2"> name of second h2</a></li>
			<!-- at the anchor point later in page, add <a name="anchorname"></a> -->
			<li>add more links as necessary</li>
		</ul>
		</div>
	</div>

!!! For every module/sction/chapter page, begin with:
	<a name="top"></a>
	<hr class="hrfade">
	<div class="inthislesson">
		<div class="innerborder">
		<h1>let's begin</h1>
		<!-- keep above title all lower case -->
		<p>quick intro sentence or two</p>
		<ul>
			<li><a href="#anchorname"> name of first h2</a></li>
			<li><a href="#anchorname2"> name of second h2</a></li>
			<!-- at the anchor point later in page, add <a name="anchorname"></a> -->
			<li>add more links as necessary</li>
		</ul>
		</div>
	</div>


!!! Images
	To create an image with a caption and lightbox.
<!-- For the caption to work, you have to have the whole image inside a div. If you already have a div for another purpose (ie compareimage) then that will do fine. Free standing images just need a plain div with no class. -->
<div>
	<a rel="lightbox" href="">
		<img src="" alt="" class="">
		<div class="desc">
			<p class="caption">
			</p>
		</div>
	</a>
</div>

Parts contained within the above:
	Add border and resize images:
		Class name tells you how big it will be
		HTML: <img src="same file reference" alt="" class="fill in class name here">
		Markdown: ![alt text](filename?class=whatever&class=secondwhatever)
		<!-- which class you choose usually depends on relative height of image. if the image is relatively tall, use a smaller class. if image is landscape orientation, use 90 or 100. Use 45 for images that are still clear when small and are secondary importance. -->
		Classes:	image45 (45% width of display area)
					image70 (70% width of display area)
					image70v (70% class but for vertical images so they don't get too tall)
					image90 (90% width of display area)
					image100 (100% width of display area - use for images with short(er) heights and for anytime you are using COMPARE class)
					mobile (use for all mobile screen shots)
					imageex (for images inside tables of descriptions and images ie layers table)

To make images open in a lightbox (apply to almost all images):
		HTML: wrap image in a link 
<a rel="lightbox" href="file reference"><img src="same file reference" alt="" class=""></a>
		Markdown: ![alt text](filename?class=imageXX&lightbox)
		(if no class it would look like filename?lightbox instead)


To line images up horizontally, ie display in columns if there is enough display width. several parts:
		1. Wrap area in div with class compare
			<div class="compare">
		2. Wrap each individual image in another div, with class compareimage.
			<div class="compareimage">
				<a rel="lightbox" href="file reference">
					<img src="same file reference" alt="" class="compareimage,image100"> (or mobile instead of image100)
					<div class="desc">
						<p class="caption">Caption Text here.</p>
					</div>
				</a>
			</div>
				Can also add desc class to each image.
		3. Close original div
			</div>



<!-- Full example of a compare image section using mobile images. This will allow images to display next to each other if there is enough space, they will all open in lightbox, and they have captions. This would go inside of a  mobile callout section-->
<p class="pcollase">
	<!-- if you have a paragraph right above the images, add the pcollapse class to the paragraph to reduce the space below it.  -->
<div class="compare">
  <div class="compareimage">
    <a rel="lightbox" href="/user/pages/all_users/04. objects/01. markers/objects_markers_mobile_01.png">
      <img src="/user/pages/all_users/04. objects/01. markers/objects_markers_mobile_01.png" alt="markers menu" class="mobile">
      <div class="desc"><p class="caption">Map Objects Menu in the Mobile App (from tapping the button at the top-center of the map viewer screen.</p></div>
    </a>
  </div>
  <div class="compareimage">
    <a rel="lightbox" href="/user/pages/all_users/04. objects/01. markers/objects_markers_mobile_02.png">
      <img src="/user/pages/all_users/04. objects/01. markers/objects_markers_mobile_02.png" alt="markers add object menu"  class="mobile">
      <div class="desc"><p class="caption">Menu after tapping the +Add Map Item button at the bottom of the previous screen.</p></div>
    </a>
  </div>
  <div class="compareimage">
    <a rel="lightbox" href="/user/pages/all_users/04. objects/01. markers/objects_markers_mobile_03.png">
      <img src="/user/pages/all_users/04. objects/01. markers/objects_markers_mobile_03.png" alt="markers mobile 3"  class="mobile">
      <div class="desc"><p class="caption">Alternatively, long-pressing on the map viewer at a point will produce a menu that will have an option to Add Marker.</p></div>
    </a>
  </div>
</div>
<!-- end example -->

!!! Videos
	Wrap in div with class video
	<!-- just add source link -->
		<div class="video">
			<h3>Title Here</h3>
			<div class="iframe">
				<iframe class="iframe" src="" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
				</iframe>
			</div>
		</div>
Vimeo: replace iframe above with vimeo embed code. remove size, add class="iframe"

!!! Mobile Section
	To style the mobile section, build it as such:
	<div class="mobile">
		<div class="mobilecalloutimg">
        	<img src="/user/pages/all_users/MOBILE_header.png">
		</div>
		<h3>Section Title Here</h3>
		<p> add content in p tags</p>
		<p>can have multiple paragraphs</p>
	<!-- if you have screen shots to add use this (example is for 3 images, thus uses class="compareimage3" instead of class="compareimage" as you would for 2 images) --> 
		<div class="compare">
	      <div class="compareimage3"><a rel="lightbox" href=""><img src="relative link" alt="" class="mobile"><div class="desc"><p class="caption"></p></div></a></div>
	      <div class="compareimage3"><a rel="lightbox" href=""><img src="next relative link" alt="" class="mobile"><div class="desc"><p class="caption"></p></div></a></div>
	      <div class="compareimage3"><a rel="lightbox" href=""><img src=" nextrelative link" alt="" class="mobile"><div class="desc"><p class="caption"></p></div></a></div>
	<!-- end of image section -->
		</div> 
		<p>another paragraph if you want it</p>  
	</div>
<!-- end of mobile section -->

!!! Table for Examples- ie for descriptions of layers and overlays with images
	To style a table-like structure that is adaptable for smaller devices:
	Header Section:
		<hr class="hrfade">
		<!-- internal link target here -->
		    <h2>Title of Section</h2>
		<div class="tablehead">
			<div class="thl">
				<p>Description</p>
			</div>
			<div class="thr">
				<p>Examples</p>
			</div>
		</div>
	Each "row" in the table:
	<div class="descriptionarea">
		<div class="col-1">
			html content (designed for text description, can include images)
		</div>
		<div class="col-2">
			html content (designed for images)
		</div>
	</div>



!!! More Tables

div.table2, col-t1 plus col-t4
div.tablehead2
These two make a simple, two column table, with a title on the left and description on the right. Split is 33/67. Tablehead2 lines the heading bar up better. Example in config lesson.

div.table2, no tablehead
makes a three column table with no header, but it has three columns. example is the intro section of the overlays or layers pages to list the links to all the individual descriptions. 


table50 has two columns: col-t1-50 and col-t2-50 Example in Map Viewer Tour - similar to image comparison or to description area - but when you want the image to be more than 1/3 of the body

