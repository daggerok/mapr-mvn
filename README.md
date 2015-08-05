MapR practice skeleton (mvn)
============================
    # do some code...
    $ mvn clean package
    $ scp mapreduce-$n/target/mapreduce-$n-1.0-jar-with-dependencies.jar user01@maprdemo:~/mapreduce-$n.jar
    $ ssh user01@maprdemo
    $ hadoop -jar maprdemo-$n.jar ...

where $n is example project number
