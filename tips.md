For running streaming on quickstart box, the `hs` command doesn't work. But this does...

```
$ export HADOOP_HOME=/usr/lib/hadoop-mapreduce
$ hadoop jar $HADOOP_HOME/hadoop-streaming-2.6.0-cdh5.5.0.jar \
> -files mapper.py,reducer.py \
> -input /user/csds/input/* \
> -output /user/csds/outputpy \
> -mapper mapper.py \
> -reducer reducer.py
```

For convenience, this is a nice alias:

```
alias hdfs='hadoop fs'
```
