# Data Origins
This files specifies where the data files used in this repository are coming from

## *.words

nomen/adjektive come from Hamburg Dependency Treebank:

in particular, I take the 1000 most frequent nouns/adjectives from the treebank.

To replicate, download HDT v.1.0.1 in CONLL format from https://corpora.uni-hamburg.de/hzsk/de/islandora/object/treebank:hdt
Then, execute:
```bash
tar xJf hdt.tar.xf
cd hamburg-dependency-treebank-conll
grep -P "^.*\t.*\t.*\tN\tN" part_A.conll|less|cut -f 2|sort|uniq -c | sort -n|tail -1000|awk '{print $2}' > /home/timo/uni/projekte/freeverseprosody/lehre/plottingpoetry/nomen
grep -P "^.*\t.*\t.*\tADJA\tADJA" part_A.conll|less|cut -f 2|sort|uniq -c | sort -n|tail -1000|awk '{print $2}' > /home/timo/uni/projekte/freeverseprosody/lehre/plottingpoetry/adjektive
```

## *.lines

parlando.lines and soundpoetry.lines come from the (licensed!) lyrikline.org corpus using the class-wise annotation defined for our Coling2018 paper.


