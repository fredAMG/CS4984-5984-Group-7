# CS4984-5984-Group-7
Big data (Text Summarization)

Copy event folder to HDFS:
```console
[cs4984cs5984f18_team7@node00 ~]$ hadoop fs -put ~/7_NeverAgain_big /user/cs4984cs5984f18_team7/7_NeverAgain_big
```

Spark Shell command for running our WARC/CDX to JSON conversion:

```console
[cs4984cs5984f18_team7@node00 ~]$ spark2-shell -i /home/cs4984cs5984f18_team7/ArchiveSpark_sentence_extraction.scala --files /home/public/cs4984_cs5984_f18/unlabeled/lib/en-sent.bin --jars /home/public/cs4984_cs5984_f18/unlabeled/lib/archivespark-assembly-2.7.6.jar,/home/public/cs4984_cs5984_f18/unlabeled/lib/archivespark-assembly-2.7.6-deps.jar,/home/public/cs4984_cs5984_f18/unlabeled/lib/stanford-corenlp-3.5.1.jar,/home/public/cs4984_cs5984_f18/unlabeled/lib/opennlp-tools-1.9.0.jar
```

Shell command to copy JSON to home folder:

```console
[cs4984cs5984f18_team7@node00 ~]$ hadoop fs -get /user/cs4984cs5984f18_team7/7_Shooting_Las_Vegas_2017/sentences .
```

Shell command for Solr indexing (run on blacklight and not cluster)"

```console
[cs4984cs5984f18_team7@blacklight:~]$ curl 'http://blacklight.cs.vt.edu:8983/solr/big_team7/update/json?commit=true' --data-binary @solr_part-00000-382d3233-a0f1-4642-a6b7-d098f86c872a-c000.json -H 'Content-type:application/json'
