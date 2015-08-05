MapR practice (mvn)
===================
    $ git clone https://github.com/daggerok/mapr-mvn.git mapr --depth=1 && cd mapr
    $ mvn clean package
    $ java -jar mapreduce-1/target/mapreduce-1-1.0-jar-with-dependencies.jar mapreduce-1/src/test/resources/receipts.txt mapreduce-1/target/result
    $ cat mapreduce-1/target/result/part-r-00000 # check result
    
    # or on hadoop
    # do not forget build jar with java 7):
    $ scp mapreduce-1/target/mapreduce-1-1.0-jar-with-dependencies.jar user01@maprdemo:~/mr1.jar
    $ scp mapreduce-1/src/test/resources/receipts.txt user01@maprdemo:~/input
    $ ssh user01@maprdemo
    $ hadoop jar mr1.jar input result # run job (should done much faster)
    $ cat result/part-r-00000 # check result
