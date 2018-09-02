# CS4984-5984-Group-7
Big data (Text Summarization)

Spark Shell command for running our WARC/CDX to JSON conversion:

```console
[cs4984cs5984f18_team7@node00 ~]$ spark2-shell -i /home/cs4984cs5984f18_team7/ArchiveSpark_sentence_extraction.scala --files /home/public/cs4984_cs5984_f18/unlabeled/lib/en-sent.bin --jars /home/public/cs4984_cs5984_f18/unlabeled/lib/archivespark-assembly-2.7.6.jar,/home/public/cs4984_cs5984_f18/unlabeled/lib/archivespark-assembly-2.7.6-deps.jar,/home/public/cs4984_cs5984_f18/unlabeled/lib/stanford-corenlp-3.5.1.jar,/home/public/cs4984_cs5984_f18/unlabeled/lib/opennlp-tools-1.9.0.jar
```

Shell command to copy JSON to home folder:

```console
[cs4984cs5984f18_team7@node00 ~]$ hadoop fs -get /user/cs4984cs5984f18_team7/7_Shooting_Las_Vegas_2017/sentences .
```
