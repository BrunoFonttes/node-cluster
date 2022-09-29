# node-cluster

The main goal of this poc is to explore the nodejs clustering capability. For that, we use a tool from the package apache2-utils called "ab".
The "ab" is a benchmark tool which provide us metrics about the performance of our application.

Here is how to use it:

1. First of all, install it by using the following command if you are in linux:
```
sudo apt-get install -y apache2-utils
```
2. For running the tool, you must have your application running in some port of your local environment, or hosted in some public address, having that, use the following command, changing its parameters in accord to your test case:
```
ab -r -c 500 -t 10 http://127.0.0.1:8080/ 
```
the -c flag means the concurrency size, the -t flag means the amount of times the batches(previously set by the -c flag) are gonna be run. that is, for the example ahead, we are gonna run 10 batches of 500 simultaneous requests, totalizing 5000 requests.
