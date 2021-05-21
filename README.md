# FIAP - Microservices (Hands-On) | LAB 2 Kafka

---

## Run conteiner Kafka e Zookeper (Kafka e Zookeper)
> docker run -p 2181:2181 -p 9092:9092 --net=host --env ADVERTISED_HOST=$IP --env ADVERTISED_PORT=9092 --name=kafka -d spotify/kafka

## Conteiner Producer
> docker build -t producer --build-arg WEBHOOK_ARG .  
> docker run --name produtor_Kafka -p 5001:5001 --rm --net=host -d producer

> ### Config Webhook
> export WEBHOOK_ARG=$webhook  
> echo $WEBHOOK_ARG

> ### Acessar no navegador
> http://ip:5001/

## Conteiner Consumer
> docker build -t consumer --build-arg WEBHOOK_ARG .  
> docker run --name consumer_Kafka --rm --net=host -d consumer

> ### Config Webhook
> export WEBHOOK_ARG=$webhook  
> echo $WEBHOOK_ARG
 
> ### Acessar no navegador
> http://ip:5001/api/ui
