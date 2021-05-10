# Commands to slice and dice

Schneidewin: 

```bash

cd /Users/matteo/Documents/AjaxMultiCommentary/GT-commentaries-OCR

python python ~/Documents/Lace2-tools/training_set_from_tsv.py --csvFile sophokle1v3soph/sophokle1v3soph_training.tsv --imageDir /Volumes/GoogleDrive/.shortcut-targets-by-id/12W80v9RNL9hQvtqnATpvd2zdMvuySsn4/AjaxMultiCommentary/data/commentary_data/schneidewin/images/sophokle1v3soph-images/ --outputDir sophokle1v3soph/pairs/

cat sophokle1v3soph/pairs/*.txt | python ~/Documents/Lace2-tools/unique_chars.py > sophokle1v3soph/unique_chars.log
```

Campbell:

```bash
python python ~/Documents/Lace2-tools/training_set_from_tsv.py --csvFile cu31924087948174/cu31924087948174_training.tsv --imageDir /Volumes/GoogleDrive/.shortcut-targets-by-id/12W80v9RNL9hQvtqnATpvd2zdMvuySsn4/AjaxMultiCommentary/data/commentary_data/campbell/images/cu31924087948174-images/ --outputDir cu31924087948174/pairs/
```
