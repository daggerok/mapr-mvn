MapR practice (mvn)
===================
    $ git clone https://github.com/daggerok/mapr-mvn.git mapr --depth=1 && cd mapr
    $ mvn clean package
    $ java -jar mapreduce-1/target/mapreduce-1-1.0-jar-with-dependencies.jar mapreduce-1/src/test/resources/receipts.txt mapreduce-1/target/result

where $n is example project number
