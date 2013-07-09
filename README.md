color-shade
===========

C'est un outils pour créer à partir du DEM au format tif une image avec ombrage et couleurs symbolisant l'altitude.

Il est très fortement inspiré de hillshade.cpp

Compilation
===========
Testé sur debian wheezy :

```
apt-get install libmagick++-dev libgdal-dev libgdal1-dev libgdal1 libmagick++-dev libmagick++5
```

```
g++ -O3 color-shade.cpp -lMagick++  -lgdal -I/usr/include/ImageMagick/ -o color-shade
```

Pas fan de git ?

```
wget https://raw.github.com/osm-fr/color-shade/master/color-shade.cpp -O - | g++ -O3 -lMagick++  -lgdal -I/usr/include/ImageMagick/ -o color-shade
```


Usage
=====
```
./color-shade -h
```
Un example pour avoir un dégradé de couleur allant du vert clair au rouge et mettant en bleu les altitude inférieur à 0 est 
fourni dans scale.txt