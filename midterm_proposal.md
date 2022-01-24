## -1. Background
Zeek is important blabla...

Containerized Zeek is wildly used .... So we want to do so.

### Zeek Architecture

Single Instance Process Flow:
![](https://docs.zeek.org/en/master/_images/architecture.png)

Cluster Architecture:
![](https://docs.zeek.org/en/master/_images/deployment.png)

#### Possible Bottlenecks:
1. Hardware Limitation? ——zeek is single-threaded so may be not
2. every step in Process Flow
    —— we want to make sure it's process rate?


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
1. [Zeek-Osquery: Host-Network Correlation for Advanced Monitoring and Intrusion Detection](https://link.springer.com/chapter/10.1007/978-3-030-58201-2_17) :
    Our evaluation results indicate that a single Zeek instance can manage more than 870 osquery hosts and can attribute more than 96% of TCP connections to host-side applications and users in real-time.

2. [Analysing performance issues of open-source intrusion detection systems in high-speed networks](https://www.sciencedirect.com/science/article/pii/S2214212619306003?casa_token=8XsfDdqnU1QAAAAA:Hv1Zym3SBlwgFoQE4sJ1qURJleKIN7HhW6wUamBAGpJcR9LreyrbX6SpO39D61fSS-Ls-oMCc7Qo) :
    we did not consider Zeek3 due to the following reasons. First, Zeek only supports Libpcap and PF_RING

This Paper can give us many inspirations

3. [Detection of Brute-Force Attacks in End-to-End Encrypted Network Traffic](https://dl.acm.org/doi/pdf/10.1145/3465481.3470113)
    
## 4. What we have done 
