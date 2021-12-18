### Detecting Malicious Attacks Through The Network Traffic

By(Hatim Alshehri & Fahad Alnafisa)

## Abstract:
The network intrusion detection system (NIDS) has become an essential tool for detecting attacks in computer networks and protecting the critical information and systems. The effectiveness of an NIDS is usually measured by the high number of detected attacks and the low number of false alarms. Machine learning techniques are widely used for building robust intrusion detection systems, which adapt with the continuous changes in the network attacks. However, a comparison of such machine learning techniques needs more investigation to show their efficiency and appropriateness for detecting sophisticated malicious attacks.
The project goal is to detect and examine network traffic from malicious attacks by generating a machine learning model to classify the network traffic.

## What is IDS (Intrusion Detection System)?
Intrusion Detection Systems (IDS) are precisely present to prevent attacks and infiltration to Networks, which might affect the organization. They monitor network traffic for suspicious activities and issue alert in case of issues.

### Types if IDS:
* Signature-based intrusion detection– In this kind incoming attacks are compared with pre-existing database of known attacks.
* Anomaly-based intrusion detection- It uses statistics to form a baseline usage of the networks at different time intervals. They were introduced to detect unknown attacks.

Based on where they discover, they can be classified into:
* Network intrusion detection (NIDS)
* Host intrusion detection (HIDS)

## Problem Statement:
With the rise of Internet usage, it is very important to protect Networks. The most common risk to a network’s security is an intrusion such as brute force, denial of service or even an infiltration from within a network. With the changing patterns in network behavior, it is necessary to switch to a dynamic approach to detect and prevent such intrusions.

### Importance of this dataset:
Although there were few daatset available before this dataset for NIDS, but they were generated decades ago and do not provide realistic outputs. That's why this dataset had been created by Nour Moustafa to tackle existing problems like: unbalanced dataset, missing values etc.


## Data:
This data set has a hybrid of the real modern normal and the contemporary synthesized attack activities of the network traffic. Existing and novel methods are utilised to generate the features of the UNSW- NB15 data set. This data set is available [here](https://cloudstor.aarnet.edu.au/plus/index.php/s/2DhnLGDdEECo4ys?path=%2FUNSW-NB15%20-%20CSV%20Files%2Fa%20part%20of%20training%20and%20testing%20set).

*  The obtained dataset consists of over 250,000 network traffic records with 45 features.

* Field Description:

 Field Name  | Description |
 ----------- | ----------- |
| id          | unique identifier for each attack |
| dur         | Record total duration         |
| proto       | Transaction protocol      |
| service     | http, ftp, ssh, dns ..,else (-) |
| state       | The state and its dependent protocol, e.g. ACC, CLO, else (-) |
| spkts       | Source to destination packet count |
| dpkts       | Destination to source packet count |
| sbytes      | Source to destination bytes         |
| dbytes      | Destination to source bytes|
| rate        | The avrage attack rate           |
| sttl        | Source to destination time to live         |
| dttl        | Destination to destination time to live     | 
| sload       | Source packets retransmitted or dropped      |
| dload       | Destination packets retransmitted or dropped      |
| sloss       | Source packets retransmitted or dropped
| dloss       | Destination packets retransmitted or dropped     |
| sinpkt      | Source inter-packet arrival time (mSec)         |
| dinpkt      | Destination inter-packet arrival time (mSec)    |
| sjit        | Source jitter (mSec)                            |
| djit        | Destination jitter (mSec)                     |
| swin        | Source TCP window advertisement               |
| dwin        | Destination TCP window advertisement          |
| stcpb       | Source TCP sequence number                    |
| dtcpb       | Destination TCP sequence number               |
| tcprtt      | The sum of ’synack’ and ’ackdat’ of the TCP   |
| synack      | The time between the SYN and the SYN_ACK packets of the TCP |
| ackdat      | The time between the SYN_ACK and the ACK packets of the TCP |
| smean       | Mean of the flow packet size transmitted by the src         |
| dmean       | Mean of the flow packet size transmitted by the dst         |
| trans_depth | the depth into the connection of http request/response transaction |
| response_body_len | The content size of the data transferred from the server’s http service |
| ct_srv_src         | No. of connections that contain the same service and destination address in 100 connections according to the last time |
| ct_state_ttl       | No. for each state according to specific range of values for source/destination time to live       |
| ct_dst_ltm         | No. of connections of the same destination address in 100 connections according to the last time        | 
| ct_src_dport_ltm   | No of connections of the same source address  and the destination port  in 100 connections according to the last time    | 
| ct_dst_sport_ltm   | No of connections of the same destination address and the source port in 100 connections according to the last time    |
| ct_dst_src_ltm     | No of connections of the same source and the destination address in in 100 connections according to the last time   | 
| is_ftp_login       | If the ftp session is accessed by user and password then 1 else 0     | 
| ct_ftp_cmd         | No of flows that has a command in ftp session |
| ct_flw_http_mthd   | No. of flows that has methods such as Get and Post in http service        | 
| ct_src_ltm         | No. of connections of the same destination address in 100 connections according to the last time     |
| ct_srv_dst         | No. of connections that contain the same service and destination address in 100 connections according to the last time        |
| is_sm_ips_ports    |  If source equals to destination IP addresses and port numbers are equal, this variable takes value 1 else 0        |
| attack_cat | The name of each attack category. In this data set, nine categories (e.g., Fuzzers, Analysis, Backdoors, DoS, Exploits, Generic, Reconnaissance, Shellcode and Worms) |
| label | 0 for normal and 1 for attack records | 

## Tools:
* python 3.9
* pandas
* numpy
* matplotlib
* seaborn
* sikit.learn
