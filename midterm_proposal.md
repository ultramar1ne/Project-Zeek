## -1. Background

## 2. Goals
### at Least
????
### Ambitious
????

## 0. What to Evaluate
Metrics/Benchmark

#### Single Zeek Container

1. 【Packet Arrival Rate】and【Intrusion Detection Accuracy】when running Zeek on single mode
2. 【Highest packet Processing Rate】which single Zeek can maintain the above two metrics

#### Multiple Zeek Containers (Cluster)
1. 【Minimum Number of Containers】 to maintain the [Packet Arrival Rate]
2. whether 【Intrusion Detection Accuracy】will decrease as [Packet Processing Rate] increases.

## 1. Tools and Datasets
### Tools:

1. *Zeek* and *Docker* : ofc
2. TCPReplay : modify and replay packets in pcap files
3. Zeek Log Parser [github link](https://github.com/dgunter/ParseZeekLogs)
4. PcapXray [github link](https://github.com/Srinivas11789/PcapXray) : display the network topology and some high-dimension info in pcap files directly


### Datasets:
#### Pcap:
[UNSW-NB15](https://cloudstor.aarnet.edu.au/plus/index.php/s/2DhnLGDdEECo4ys?path=%2FUNSW-NB15%20-%20pcap%20files)

A widely used cyber-security dataset. Still updated now. 

Contains both classified *attacks*(DDoS, Scan, Backdoors, ...) and daily normal flows.

#### ...will be more...

