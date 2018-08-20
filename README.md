JavaScript content magnifier.

Usage:

1) Include the script:

~~~
<script type="text/javascript" src="magnifier.js"></script>
~~~

2) Create magnifier instance

~~~
var magnifier = new Magnifier();
~~~

3) Show when needed

~~~
magnifier.show();
~~~

4) Hide when not needed

~~~
magnifier.hide();
~~~

That's all.

There are also some settings which you can pass to constructor

~~~
{
zoom: 2
shape: square | circle
size: 200
}
~~~

Or set aftewards

~~~
magnifier.setZoom(2);
magnifier.setShape('circle');
magnifier.setSize(300);
~~~

There are also couple events which you may find usefull

1) You may want to remove some elements from magnfication:

~~~
magnifier.on('prepareContent', function(magnifierContent) {
    $('.some-selector', magnifierContent).remove();
});
~~~

2) In some cases you may want to sync scroll positions for scollable areas:

~~~
magnifier.on('syncScrollBars', function(magnifierContent) {
  $('div.scrollable-area', magnifierContent).scrollTop($('div.scrollable-area').scrollTop());
});
~~~


Have fun. Send PR if you find any glitches or want to make improvements.

:)
