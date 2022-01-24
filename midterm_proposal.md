## -1. Background
Zeek is important blabla...

Containerized Zeek is wildly used .... So we want to do so.

## 0. Goals
### at Least
????
### Ambitious
????

## 1. What to Evaluate
Metric/Benchmark

### Definition
1. Traffic Rate : 

    Number of Packets Sent to Zeek per minute
3. Packet Arrival Rate:

    (Number of packets shown in Zeek's log) / (Total Number)

4. Intrusion Detection Accuracy: 

    (Correctly Detected Intrusions) / (Total Number of Intrusions)


#### Single Zeek Container

1. 【Packet Arrival Rate】
2. 【Intrusion Detection Accuracy】
3. 【Highest Traffic Rate】with which single Zeek can maintain the above two metrics

#### Multiple Zeek Containers (Cluster?)
1. whether 【Packet Arrival Rate】will decrease as [Traffic Rate] increases.
2. whether 【Intrusion Detection Accuracy】will decrease as [Traffic Rate] increases.
3. if so,【Minimum Number of Containers】 to maintain the best performance
【Load Balance?】 other bottle neck?

## 2. Tools and Datasets
### Tools:

1. *Zeek* and *Docker* : ofc
2. TCPReplay : modify and replay packets in pcap files
3. Zeek Log Parser [github link](https://github.com/dgunter/ParseZeekLogs)
4. PcapXray [github link](https://github.com/Srinivas11789/PcapXray) : display the network topology and some high-dimension info in pcap files directly


### Datasets:
#### Pcap:
1. [UNSW-NB15](https://cloudstor.aarnet.edu.au/plus/index.php/s/2DhnLGDdEECo4ys?path=%2FUNSW-NB15%20-%20pcap%20files)

    A widely used cyber-security dataset, still updated now,

    contains both classified *attacks*(DDoS, Backdoors, ...) and daily normal network flows.


## 3. Related Works
Paper?

## 4. What we have done 
