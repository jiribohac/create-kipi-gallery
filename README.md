# create-kipi-gallery
a bash script to create a HTML gallery using a theme from kipi-plugins HTML-export

In the past, I started creating my photo galleries using KIPI-plugin called HTML Export. First I used kphotoalbum and later gwenview to invoke the plugin and convert my pictures to a HTML gallery.
I created my custom theme for this plugin, called floating-cards. See an
example here: http://jjjjj.boha.cz

Over the years, as I upgraded my system, I kept coming across new bugs in different parts of the toolchain, which prevented me from updating my photo gallery.
The last straw was a recent removal of the HTML Export plugin from the kipi-plugins suite. The code, including my theme, has been moved to the digikam project. I have no intention to use digikam. Why on Earth had I been using hundreds of megabytes of buggy code for something as simple as a HTML gallery?

So I hacked this simple bash script. 

It takes a directory of photos as an argument and creates a HTML gallery using a theme from the original kipi-plugins.
It creates the gallery.xml file and uses xsltproc to generate the HTML code. It uses imagemagick to process the images.

*Creating a simple HTML gallery in the current directory is as simple as:
create-kipi-gallery /path/to/a/directory/with/pictures*

Optionally, you can use a plain text index file to specify the order/subset and optionally descriptions of images. If no index file is present, the script uses all image files sorted alphabetically. If no index file is present or the index file does not include a description, the description is taken from the exif.

"create-kipi-gallery -h" lists all available options.
If you don't like the default settings, just edit them near the top of the script.


Enjoy. Improve. Share.
