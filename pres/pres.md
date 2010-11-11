HTML5 Video 101
===============
* Exploring the possibilities of the HTML5 video element
* Interactive session
* At the last moment…
* Introduction
* Examples
* How the VPRO is (not) using it

About me
========
<img src="../bin/hay.jpg" height="200" />

* Frontend developer VPRO
* Cultural advisor Wikimedia
* [@huskyr](http://twitter.com/huskyr)
* [github](http://github.com/hay/html5video)

VPRO
====
<img src="../bin/vpro.png" height="100" />

* Public broadcaster
* Television, Radio, Guide, Digital
* Digital since 1994
* Audio / video core business
* Open source (Apache, CouchDB)

VPRO ca 1994
============
<img src="../bin/vproweb.gif" height="600" />

VPRO 2010
=========
<img src="../bin/vprosite.png" height="600" />

Why use HTML5 `<video>`?
========================
* First-class citizen in HTML
    * Just use like `<img>`
    * [Example](../rotate/index.html)
* Native to the browser
    * No plugin hell
* No DRM
* One codebase for everything
* Multiple competing implementations
    * If you don't like `<video>` in browser x, switch to browser z
* Better performance (in some browsers, some systems)
* Ready for the (mobile) future
* Works on iPad :)

Other cool stuf
===============
* [Stuff from Mozilla's Paul Rouget](http://paulrouget.com/)
* [Green screen](https://people.mozilla.com/~prouget/demos/green/green.xhtml)
* [SVG filters](https://people.mozilla.com/~prouget/demos/mashup/video.xhtml)
* [Subtitles](https://people.mozilla.com/~prouget/demos/srt/index2.xhtml)

Introduction
============
* [Dive into HTML5](http://diveintohtml5.org/video.html)
* [RTFM](http://www.whatwg.org/specs/web-apps/current-work/multipage/video.html#video)

Code
====
    <video src="video.ogg" controls>I can not haz HTML5 video :(</video>
    
<video src="../bin/video.ogg" controls="controls"></video>

Code
====
    <video src="video.ogg" width=640 height=480 preload autoplay controls/>
    
<video src="../bin/video.ogg" controls="controls" width="640" height="480"></video>

Code
====
* As simple as that? 
* No :(

Codecs, codecs, codecs
======================
* OGG Theora (Firefox / Opera / Chrome)
* H264 / MPEG4 (Safari / IE / Chrome)
* WebM (Firefox / Opera / Chrome)

OGG / WebM
==========
* Open source
* Patent free (probably)
* Used on Wikipedia

H264 / MPEG4
============
* Closed
* Might need a license
* Works on iOS

Real world code
===============
    <!-- From http://diveintohtml5.org/video.html#markup -->
    <video width="320" height="240" controls> 
        <source src="pr6.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'> 
        <source src="pr6.webm" type='video/webm; codecs="vp8, vorbis"'> 
        <source src="pr6.ogv" type='video/ogg; codecs="theora, vorbis"'> 
        <!-- Some Flash fallback -->
    </video>
    
Making things easier
====================
<span style="font-size:150px;margin:0 auto;">JavaScript</span>

Using JavaScript
================
[Example](../controls/index.html)

Video at VPRO
=============
* Lots of video
* Most of it in Windows Media formats
* Some of it in H264
* Realvideo :)
* So.. no HTML5? 

Canvas
======
* It gets more complicated
* Silverlight player for stuff on UitzendingGemist.nl
* But not everything is on UitzendingGemist.nl…
* Two different players?
* Different interfaces?

Abstraction
===========
* Abstract away what's video and what's a certain technology
* 'duration', 'currentTime', 'vidpos', etc
* We need a generic API for video interfacing

Surprise…
=========
<span style="font-size:150px;margin:0 auto;">HTML5 `<video>`</span>

API
===
* A generic API for controlling videos
* Standard events

How?
====
* One generic jQuery plugin: `jquery.htmlplayer`
* Lots of canvas plugins that abstract away specific technology to generic API
    * `jquery.slmediacanvas`
    * `jquery.ugslmediacanvas`
    * `jquery.htmlvideomediacanvas
* A little CSS, a few images
* [There you have it!](http://localhost/frontend/trunk/htmlplayer/doc/tester/)

Real world
==========
* [Holland Doc](http://www.hollanddoc.nl)
* [Labyrint)(http://vpro.nl/labyrint)
* [Kiesop3](http://kiesop3.vpro.nl)
* [Geschiedenis](http://geschiedenis.vpro.nl)