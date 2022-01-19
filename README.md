## Project Title: Evaluating Zeek throughput when deployed on containers

Zeek is an IDS that helps secure enterprise networks by protecting against threats such as SSH Brute Forcing. In this project we will evaluate the scaling properties of Zeek when they are deployed within docker containers. 

We will start by running Zeek inside of a container (zeek-container). Then we will select a few attacks and verify their detection on the Zeek IDS. Until this point we will operate with one Zeek instance and evaluate what packet arrival rate it can sustain. Once done, we will try to measure the number of zeek-container instances required to sustain a given packet arrival rate. 
![](http://152.136.116.14:1023//uploads/upload_2ff020beaff9272b536f4a043242ce23.png)

Fortunately, Zeek provides many pcap traces for testing purposes. We will use mergecap to merge multiple such packet traces (one after another) to increase the trace size. We will use tcpreplay to generate replay traffic. Finally, we will evaluate whether there is a decrease in accuracy due to an increase in packet processing rate.


Prerequisites: Containers and Network Security
