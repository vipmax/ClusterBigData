MESOS + HDFS + SPARK CLUSTER
===========================
cd vms

vagrant up

wait 5 minutes

vagrant ssh controlvm

cd project/ansible/

ansible-playbook mesos.yml 

ansible-playbook hdfs.yml 

ansible-playbook spark.yml 

http://node1:5050  	mesos

http://node1:50070	hdfs

http://node1:8080	spark?

cd /opt/spark/bin/

sudo ./spark-shell --executor-memory 512m --total-executor-cores 4

