# Load Balancing in Docker Swarm Mode

This is a simple project in which we are combining load balancing with docker swarm.


The cluster look like this :

![DEMO](https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/cluster.png)

# Configuring the nodes :

We start by enabling swarm mode, and defining the leader

![DEMO](<<<<<<<https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/_1.png)

We then, get the token for joining workers :

![WORKER](https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/_2.png)

We check the nodes status :

![STATUS_NODE](https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/_3.png)

We create the service with 3 replicas

![Service](https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/_4.png)


# Configuring the load balancer :

we start by initializing a new swar mode :

![LOAD_Swarm](https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/_5.png)

We configure nginx :

![NGINX_CONF](https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/_6.png)

We create service :

![NGINX_SERVICE](https://github.com/ayoubensalem/LoadBalancing-docker-swarm/blob/master/demo/_7.png)

You can test that the load balancer is working, by changing the `/usr/share/nginx/index.html` in each container node.




# Maintainer

> Ayoub Ed-dafali
