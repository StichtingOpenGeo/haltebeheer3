Productie van Vectortiles
=========================

```
java -jar chb2shp-1.0-SNAPSHOT-all.jar
ogrmerge.py -f VRT -o merged.vrt *shp
ogr2ogr -f MBTILES -t_srs EPSG:3857 -s_srs EPSG:28992 -dsco MINZOOM=13 -dsco MAXZOOM=22 quays.mbtiles merged.vrt
```

Vectortiles serveren kan met https://github.com/consbio/mbtileserver
