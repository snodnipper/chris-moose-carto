spritezero --retina "sprite@2x" ./xmas

spritezero "sprite" ./xmas

-------

https://snodnipper.github.io/chris-moose-carto/sprite <- stick that in Maputnik

Note, the actual resources are:
https://snodnipper.github.io/chris-moose-carto/sprite.png
https://snodnipper.github.io/chris-moose-carto/sprite@2x.png

Just some notes that might be of interest:

We can easily make the images with:

spritezero --retina "sprite@2x" ./xmas

spritezero "sprite" ./xmas

Getting it available on github requires some special magic:

https://github.com/snodnipper/chris-moose-carto/tree/gh-pages is a special branch.  Essentially, it must not have any history or else it won’t work.

Updating https://github.com/snodnipper/chris-moose-carto won’t have any direct effect.

To republish we would do something like this:

git clone git@github.com:snodnipper/chris-moose-carto.git
git checkout --orphan gh-pages
(the orphan removes history)
git add .
git commit -m "add xmas carto"
git push -f
