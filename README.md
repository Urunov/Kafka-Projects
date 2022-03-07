1. sudo apt-get update

2. sudo apt-get install openjdk-8-jdk

3. sudo apt-get install zookeeperd

4. sudo systemctl status zookeeper

5. sudo systemctl start zookeeper

6. sudo systemctl enable zookeeper

sudo apt-get install net-tools

sudo netstat -tulpen | grep 2181

mkdir Downloads

cd Downloads

wget https://dlcdn.apache.org/kafka/3.1.0/kafka_2.12-3.1.0.tgz

sudo mkdir /opt/kafka

wget https://dlcdn.apache.org/kafka/3.1.0/kafka_2.12-3.1.0.tgz

sudo mkdir /opt/kafka

sudo tar xvzf kafka_2.12-3.1.0.tgz -C /opt/kafka

sudo nano /etc/profile

export KAFKA_HOME="/opt/kafka/kafka_2.12-3.1.0"

export PATH="$PATH:${KAFKA_HOME}/bin"

tail /etc/profile

sudo nano ~/.bashrc

alias sudo='sudo env PATH="$PATH"'

sudo reboot

echo $KAFKA_HOME
echo $HOME

sudo ln -s $KAFKA_HOME/config/server.properties /etc/kafka.properties

sudo kafka-server-start.sh /etc/kafka.properties

kafka-topics.sh --create --topic qqb-topic --bootstrap-server localhost:9092

-> Producer: 
kafka-console-producer.sh --topic qqb-topic --bootstrap-server localhost:9092

-> Consumer: 

kafka-console-consumer.sh --topic qqb-topic --from-beginning --bootstrap-server localhost:9092



