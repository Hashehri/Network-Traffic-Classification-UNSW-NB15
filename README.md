# Detecting Malicious Attacks Through The Network Traffic

By(Hatim Alshehri & Fahad Alnafisa)

# Abstract:
The network intrusion detection system (NIDS) has become an essential tool for detecting attacks in computer networks and protecting the critical information and systems. The effectiveness of an NIDS is usually measured by the high number of detected attacks and the low number of false alarms. Machine learning techniques are widely used for building robust intrusion detection systems, which adapt with the continuous changes in the network attacks. However, a comparison of such machine learning techniques needs more investigation to show their efficiency and appropriateness for detecting sophisticated malicious attacks.
The project goal is to detect and examine network traffic from malicious attacks by generating a machine learning model to classify the network traffic.


# Data:
This data set has a hybrid of the real modern normal and the contemporary synthesized attack activities of the network traffic. Existing and novel methods are utilised to generate the features of the UNSW- NB15 data set. This data set is available [here](https://cloudstor.aarnet.edu.au/plus/index.php/s/2DhnLGDdEECo4ys?path=%2FUNSW-NB15%20-%20CSV%20Files%2Fa%20part%20of%20training%20and%20testing%20set).

*  The obtained dataset consists of over 250,000 network traffic records with 45 features.

* Field Description:

#| Field Name  | Description |
-| ----------- | ----------- |
1| id          | unique identifier for each attack |
2| dur         | Record total duration         |
3| proto       | Transaction protocol      |
4| service     | http, ftp, ssh, dns ..,else (-) |
5| state       | The state and its dependent protocol, e.g. ACC, CLO, else (-) |
6| spkts       | Source to destination packet count |
7| dpkts       | Destination to source packet count |
8| sbytes      | Source to destination bytes         |
9| dbytes      | Destination to source bytes|
10| rate        |                                     |
11| sttl        | Source to destination time to live         |
12| dttl        | Destination to destination time to live     | 
13| sload       | Source packets retransmitted or dropped      |
14| dload       | Destination packets retransmitted or dropped      |
15| sloss       | Source packets retransmitted or dropped
16| dloss       | Destination packets retransmitted or dropped     |
17| sinpkt      | Source inter-packet arrival time (mSec)         |
18| dinpkt      | Destination inter-packet arrival time (mSec)    |
19| sjit        | Source jitter (mSec)                            |
20| djit        | Destination jitter (mSec)                     |
21| swin        | Source TCP window advertisement               |
22| dwin        | Destination TCP window advertisement          |
23| stcpb       | Source TCP sequence number                    |
24| dtcpb       | Destination TCP sequence number               |
25| tcprtt      | The sum of ’synack’ and ’ackdat’ of the TCP   |
26| synack      | The time between the SYN and the SYN_ACK packets of the TCP |
27| ackdat      | The time between the SYN_ACK and the ACK packets of the TCP |
28| smean       | Mean of the flow packet size transmitted by the src         |
29| dmean       | Mean of the flow packet size transmitted by the dst         |
30| trans_depth | the depth into the connection of http request/response transaction |
31| response_body_len | The content size of the data transferred from the server’s http service |
32| ct_srv_src     | No. of connections that contain the same service (4) and destination address (3) in 100 connections according to the last time (26)
33| attack_cat | The name of each attack category. In this data set, nine categories (e.g., Fuzzers, Analysis, Backdoors, DoS, Exploits, Generic, Reconnaissance, Shellcode and Worms) |
34| label | 0 if it is normal otherwise 1 | 

