# Go Kafka Example

this is a basic go kafaka crud designed using sharama package from IBM, which is most stable version abalible on internet...

<h2> docker-compose steps </h2>

1. Install Docker and Docker Compose

2. Run `docker-compose up -d` in the root directory. This will start Apache Kafka and Zookeeper

3. Install dependencies

4. Run go run `producer/producer.go` to start the producer which is a REST API listening on port 3000

5. Run go run `worker/worker.go` to start the consumer

## Testing

Send a POST request to `localhost:3000`

This will produce a message in Apache Kafka and the consumer respond accordengly...

```
curl --location --request POST '127.0.0.1:3000/api/v1/comments' `
--header 'Content-Type: application/json' `
--data-raw '{ "text":"HI MOM" }

curl --location --request POST '127.0.0.1:3000/api/v1/comments' `
--header 'Content-Type: application/json' `
--data-raw '{ "text":"HI DAD" }'
```
