The most common scenario for connecting to containers is an application connecting to a data-store. The key aspect when creating a link is the name of the container. All containers have names, but to make it easier when working with links, it's important to define a friendly name of the source container which you're connecting to.

Start Data Store
Run a redis server with a friendly name of redis-server which we'll connect to in the next step. This will be our source container.

`docker run -d --name redis-server redis`{{execute}}

Redis
Redis is a fast, open source, key-value data store.
