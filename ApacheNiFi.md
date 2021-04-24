###Data flow 
Flow of data from one source to another
###Data Pipeline 
That is movement and transformation of data/content from Source to Destination
###ETL - Extract Transform Load
Data pipeline -> Batch(пакет) / Stream
ETC -> Batch

####In natural way of organizing dataflow we have 4 v's problem:
- Volume(Объём) -> refers to the vast amount of data generated every second
- Velocity(Скорость) -> refers to the speed at which new data is generated and the speed at which data moves around
- Variety(Разнообразие) -> refers to the different types of data we cat now use
- Veracity(Правдивость) -> refers to the messiness or trustworthiness of the data

####Considerations:
- Support for multiple data format - CSV, Json, Plaintext, Images, Videos, etc.
- Support for various types of sources and destinations : FTP, HTTP, SQL, NoSQL, Cache, SearchEngine and etc.
- Scalable and reliable for large volume and high-velocity data
- You should also consider Data Cleansing and Data Validation logics

C этими всеми проблемами мы идём к Apache NiFi и решаем их

NiFi was build to automate the flow of data between systems. It can propagate any data content from any source to any destination.

#Instalation 
```https://techexpert.tips/apache-nifi/apache-nifi-installation-ubuntu-linux/```
#Посмотреть если возьмут
https://videoportal.epam.com/video/8JYElGJd

У него есть графический интерфейс похожий на draw.io в котором ты можешь конфигурировать data flow

Core NiFi Terminologies
- NiFi is based on Flow Based Programming(FBP)
- FBP - app is a networks of "black box" processes naturally component-oriented
- NiFi consists of atomic elements which can be combined to groups to build a data flow
- NiFi consists of processors and Process Groups
####Processor
- atomic elements in NiFi which can do some simple tasks
- NiFi has more then 300 Processors
- Each Processor in NiFi is unique in it's own way

#####What a processor can do?
- We have tons of Data Source and Data Sink Processors
- The Source and Sink can be anything - SQL, NoSQL, AWS Entities(S3, DynamoDB) and etc.
- NIFI have processors for all your data needs
- NiFi Supports custom processors as well

#####FlowFile = Actual Data
