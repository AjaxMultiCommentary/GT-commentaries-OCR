# OCR Ground Truth for Historical Commentaries

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

The dataset OCR ground truth for historical commentaries (GT4HistComment) was created from the public domain subset of scholarly commentaries on Sophocles' *Ajax*. Its main goal is to enable the evaluation of the OCR quality on printed materials that contain a mix of Latin and polytonic Greek scripts. It consists of five 19C commentaries written in German, English, and Latin, for a total of 3,356 GT lines.

## Data

GT4HistComment are contained in `data/`, where each sub-folder corresponds to a different publication (i.e. commentary). For each each commentary we provide the following data:
- `<commentary_id>/GT-pairs`: pairs of image/text files for each GT line
- `<commentary_id>/imgs`: original images on which the OCR was performed

The OCR output produced by the Kraken + Ciaconna pipeline was manually corrected by a pool of annotators using the [Lace platform](https://github.com/brobertson/Lace2/). In order to ensure the quality of the ground truth datasets, an additional verification of all transcriptions made in Lace was carried out by an annotator on line-by-line pairs of image and corresponding text.

## Counts

Line, word and char counts for each commentary are indicated in the following table. Detailled counts for each region can be found [here](https://docs.google.com/spreadsheets/d/1BxtB38WbB1fFplp5mVncfHPH77Z5Z3dZT_0akFTxr0E/edit?usp=sharing).

| type        | Commentary  | id                        | Languages      | year | lines | words | all chars | greek chars|
|-------------|-------------|---------------------------|----------------|------|-------|-------|-------|-------|
| groundtruth | campbell    | cu31924087948174          | Greek, English | 1881 | 464   | 2987  | 14291 | 3566  |
| groundtruth | jebb        | sophoclesplaysa05campgoog | Greek, English | 1896 | 324   | 2418  | 10986 | 2805  |
| groundtruth | lobeck      | bsb10234118               | Greek, Latin   | 1835 | 202   | 1491  | 7917  | 2786  |
| groundtruth | schneidewin | sophokle1v3soph           | Greek, German  | 1853 | 382   | 1599  | 8436  | 2191  |
| groundtruth | wecklein    | Wecklein1894              | Greek, German  | 1894 | 211   | 1912  | 9556  | 3268  |
| training    | lobeck      | bsb10234118               | Greek, Latin   | 1835 | 574   | 2943  | 16081 | 5344  |
| training    | Schneidewin | sophokle1v3soph           | Greek, German  | 1853 | 583   | 2970  | 16112 | 3269  |
| training    | jebb        | sophoclesplaysa05campgoog | Greek, English | 1896 | 561   | 4102  | 19141 | 5314  |



## Commentary overview


|        ID     | Commentator     | Year | Languages | Image source | Line example |
|---------------|-----------------|------|-----------|--------------|--------------|
| [bsb10234118](./data/bsb10234118/)   | Lobeck [1]      | 1835 | Greek, Latin |[BSB](http://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb10234118-7)      | ![](data/bsb10234118/GT-pairs/bsb10234118_0096_28.png)|
|[sophokle1v3soph](data/sophokle1v3soph)| Schneidewin [2] | 1853  | Greek, German | [Internet Archive](https://archive.org/details/sophokle1v3soph/page/n49/mode/2up) | ![](data/sophokle1v3soph/GT-pairs/sophokle1v3soph_0140_30.png)|
| [cu31924087948174](./data/cu31924087948174/) | Campbell [3]    | 1881  | Greek, English | [Internet Archive]( https://archive.org/details/cu31924087948174) | ![](data/cu31924087948174/GT-pairs/cu31924087948174_0063_70.png) |
| [sophoclesplaysa05campgoog](./data/sophoclesplaysa05campgoog/) |Jebb [4] | 1896  | Greek, English | [Internet Archive](https://archive.org/details/sophoclesplaysa05campgoog) | ![](data/sophoclesplaysa05campgoog/GT-pairs/sophoclesplaysa05campgoog_0136_55.png) |
| [Wecklein1894](data/Wecklein1894/)  | Wecklein [5]  | 1894 [5] | Greek. German | internal | ![](data/Wecklein1894/GT-pairs/Wecklein1894_0087_6.png) |  

### Commentary editions used:

- [1] Lobeck, Christian August. 1835. *Sophoclis Aiax*. Leipzig: Weidmann.
- [2] Sophokles. 1853. *Sophokles Erklaert von F. W. Schneidewin*. Erstes Baendchen: Aias. Philoktetes. Edited by Friedrich Wilhelm Schneidewin. Leipzig: Weidmann.
- [3] Lewis Campbell. 1881. *Sophocles*. Oxford : Clarendon Press.
- [4] Wecklein, Nikolaus. 1894. *Sophokleus Aias*. München: Lindauer.
- [5] Jebb, Richard Claverhouse. 1896. *Sophocles: The Plays and Fragments*. London: Cambridge University Press.

## Acknowledgements

Data in this repository were produced in the context of the Ajax Multi-Commentary project, funded by the Swiss National Science Foundation under an Ambizione grant [PZ00P1\_186033](http://p3.snf.ch/project-186033).

Contributors: Carla Amaya (UNIL), Sven Najem-Meyer (EPFL), Matteo Romanello (UNIL), Bruce Robertson (Mount Allison University).
