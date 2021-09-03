# This is a very simple react client.
# Several changes are needed for you to use it against the events API:

1. The k8s internal service must changed to a LoadBalancer and use port 80 so it can be accessed outside the cluster
1. The k8s SERVER environment variable in the existing external deployment must be modified from port 8082 to the new port 80
1. The .env file in the root of the react application must be modified to use the LoadBalancer's external IP in place of localhost

# You will need to create a Dockerfile that:

1. Uses the builder pattern
1. Copies the /build folder and all its contents from the transient builder image to a static web server (e.g. nginx)

