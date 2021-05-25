# kafka-alura
Repositório com exercícios da Formação Apache Kafka da Alura. O projeto desse curso consiste em um e-commerce.

Status: Em desenvolvimento

## 💻 Pré-requisitos
* Java
* Instalar o kafka (Faça o download em  kafka.apache.org)

Utilizando o Windows:
No prompt de comando, após fazer o download:

1 - descompactar o tgz: 
```
tar zxf {nome do arquivo}
```

```
tar zxf kafka_2.13-2.7.0.tgz
```
2 - mova o Kafka para C:/Kafka

3 - executar zookeper
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
- start kafka
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

## :star2: Comandos úteis
- Para criar tópicos:
```
.\bin\windows\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic NOME_DO_TOPICO
```
- Listar tópicos:
```
.\bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092 
```

- Criar o Produtor/Enviar mensagens:
```
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic NOME_DO_TOPICO
```
- Criar o consumidor:
```
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic NOME_DO_TOPICO
```
- Consumidor que recebe todas as mensagens desde o começo:
```
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic TestTopic --from-beginning
```
- Descrever tópicos
```
.\bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --describe
```
- Alterar numero de partições:
```
.\bin\windows\kafka-topics.bat --alter --zookeeper localhost:2181 --topic NOME_DO_TOPICO --partitions numeroDePaticoes
```
- Analisar grupos de consumo:
```
.\bin\windows\kafka-consumer-groups.bat --all-groups --bootstrap-server localhost:9092 --describe
```
