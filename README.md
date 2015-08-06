MapR practice (mvn)
===================
    $ git clone https://github.com/daggerok/mapr-mvn.git mapr --depth=1 && cd mapr
    $ mvn clean package -pl mr1
    $ java -jar mr1/target/mr1-1.0-jar-with-dependencies.jar mr1/src/test/resources/receipts.txt mr1/target/result
    $ cat mr1/target/result/part-r-00000 # check job result
    
now try with hadoop:

    $ scp mr1/target/mr1-1.0-jar-with-dependencies.jar user01@maprdemo:~/mr1.jar
    $ scp mr1/src/test/resources/receipts.txt user01@maprdemo:~/in1
    $ ssh user01@maprdemo
    $ hadoop jar mr1.jar in1 out1 # job should be done much faster
    $ cat out1/part-r-00000 # verify result

get more information about MapR here: https://www.mapr.com/
