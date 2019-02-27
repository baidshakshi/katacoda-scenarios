With a link created, applications can connect and communicate with the source container in the usual way, independent of the fact both services are running in containers.

#### Example Application
Here is a simple node.js application which connects to redis using the hostname redis.

`docker run -d -p 3000:3000 --link redis-server:redis katacoda/redis-node-docker-example`{{execute}}

#### Test Connection
Sending an HTTP request to the application will store the request in Redis and return a count. If you issue multiple requests, you'll see the counter increment as items are persisted.

`curl docker:3000`{{execute}}
