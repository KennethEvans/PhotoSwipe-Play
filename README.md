# PhotoSwipe Play

This project contains an implementation of PhotoSwipe that has a Play button.  It consists of a website and a simple implementation of a gallery including some sample images (which are copyrighted).  It was created because the PhotoSwipe GitHub site (https://github.com/dimsemenov/photoswipe) indicates they are not planning to include a play button, and I could find no usable examples on the web.

This implementation appears to work for me.  I do not spend a lot of time developing either Javascript or CSS, and I do not have an intimate knowledge of PhotoSwipe, so it possibly could be done better.  It has been tested on Windows 10 with Chrome, Edge, and Internet Explorer 11, and on my Android phone.

Perhaps this site will evolve with contributions from others.

This version was modified from "PhotoSwipe - v4.1.2 - 2017-04-05", available at https://github.com/dimsemenov/photoswipe.  More information about PhotoSwipe is available there and at https://photoswipe.com/.

This repository is based on an Eclipse Javascript project. You can ignore the project files and just use the website directory (gallery-playbutton).  You should be able to copy it somewhere and open index.html in a browser.

**Gallery**

The sample website is under gallery-playbutton.  It has an images directory and an _index.html_ that has a simple implementation of a gallery, no bells and whistles.

**Skin**

The play button is implemented with a different skin, named _play-skin_, that replaces the _default-skin_.  These files include an enhanced _play-skin.svg_ and _play-skin.png_, which contain play and pause images.

**Files**

* _index.html_

    Use the new CSS and Scripts:

    >\<link rel="stylesheet" href="photoswipe.css"\>
    > 
    > \<link rel="stylesheet" href="play-skin/play-skin.css"\>
    >
    >\<script src="photoswipe.min.js"\>\</script\>
    >
    >\<script src="photoswipe-ui-play.min.js"\>\</script\>


    
    Add the play button (after the zoom button):
    > \<button class="pswp__button pswp__button--play" title="Play/Pause"\>\</button\>'

    Use the new template:

    > var gallery = new PhotoSwipe( pswpElement, PhotoSwipeUI_Play, items, options);
  
 **New Options**

* The slide duration in milliseconds (default is 3000):

    > playInterval: 5000,

* Whether to use the play button or not (default is true):

   > playEl: false,

**Implementation**

The main part of the implementation is to add a Play module to photoswipe.js and change the CSS to configure the play button and to change it to play or pause.

All of the files with a default in the name have been renamed to use play instead.  _photoswipe.js_ and _photoswipe.css_ are new implementations with the same name as the old ones.  You can use the new ones with the default skin, and they will work.  (But there will not be a play button, and the new functionality will not be accessed.)  That is, they are backward compatible.

To see the changes in more detail, do a diff on the files compared to the former ones.  The changes are in a small number of isolated places.



    




