Redis
=================

Introduction
---------

This is a small rails application to demonstrate how redis is used in order to aid my own learning.

About Redis
---------

Redis is an open source, advanced key-value store. It is a non-sql database used for building high-performance applications.

Using Redis for the first Time
---------

The first thing I did after setting up the rails application was to add the redis gem to the gemfile. This allowed me to play around with
the a redis client in the rails console.

```
redis = Redis.new(:host =>'localhost', :post => 6379)
```
Redis will automatically connect to localhost:6379(the default) so it is not necessary to include the :post key-value pair.

The Redis server also has to be running in order to create an instance of a Redis Client.

```
redis-server
```
The above command will run the server.

In the rails console now, you can set a kew-value pair.

```
> redis.set('superman', 'clark kent')
=> "OK"
```
and use the 'get' method to retrieve the value for redis:

```
> redis.get('superman')
=> "clark kent"
```