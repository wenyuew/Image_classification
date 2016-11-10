# image_classification-OCR-
use tensor flow's inception v3 to classify handwritten letters 



convert png to jpg
find . -iname '*.png' | while read i; do mogrify -format jpg "$i" && rm "$i"; echo "Converted $i to ${i%.*}.jpg"; done


remove files which has fewer than 20 images, because Inception v3 models only work on the files of more than 20 images. 
