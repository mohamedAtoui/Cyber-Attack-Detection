# Cyber Attack Detection

## Introduction

In the realm of digital information, cybersecurity stands as a pivotal defense against the ever-evolving landscape of cyber threats. This project was launched in response to the substantial cybersecurity challenges that companies encounter, underscoring the urgent need for more sophisticated and adaptable threat detection systems. This initiative emerges from the necessity to address increasing vulnerabilities within network systems, which pose significant risks to personal, corporate, and governmental data.

## Project Overview

The primary aim of our project is to develop a robust model that employs machine learning techniques to identify, analyze, and predict potential cybersecurity threats in network traffic. By integrating theoretical knowledge with practical application, we created a system capable of discerning between benign and malicious traffic, thereby facilitating a proactive approach to cybersecurity.

## Objectives

1. To Apply Machine Learning in Cybersecurity: Utilize various machine learning algorithms to analyze network traffic data, improving the accuracy of threat detection.
2. To Enhance Threat Detection Capabilities: Develop a model that not only detects known types of attacks but also predicts new potential threats based on traffic behavior and anomalies.
3. To Reduce False Positive Rates: Fine-tune the detection mechanisms to distinguish more effectively between harmful and harmless activities, reducing operational disruptions caused by false alarms.



## Problem Addressed
The project addresses the critical challenge of increasing cybersecurity threats and the inadequacies of traditional detection systems in adapting to new attack vectors. With cyber threats becoming more sophisticated, there is a pressing need for adaptive and dynamic systems that can learn from ongoing activities and evolve with the threats. Our project aims to fill this gap by providing an intelligent, learning-based solution that enhances security measures and keeps pace with the rapid developments in cyber attack methodologies.

## Installation and Setup 
To run this project, you will need Python installed on your machine along with the following Python libraries:
- Pandas
- NumPy
- Matplotlib
- scikit-learn

You can install these packages using pip: (pip install numpy)


## Methodology
The methodology of our project is structured to integrate machine learning with cybersecurity practices effectively. Our approach involves several key phases: data acquisition, preprocessing, model selection, training, evaluation, and deployment. Each phase is crucial for the development of a reliable and efficient system that can predict and identify potential cybersecurity threats in network traffic.

## Data Preprocessing
In the data preprocessing phase, we undertook a careful process to refine our dataset, ensuring it was optimally structured for efficient and effective analysis. This involved selecting specific columns that were most relevant to the goals of our project while removing others that provided less value for threat detection. Our selection was based on the columns' relevance to identifying patterns and anomalies in network traffic that could indicate potential security threats.

## Columns Selected:

1. 'originp', 'responp': These columns, representing originating and responding ports, are critical as they help identify standard and anomalous communication patterns between devices.
2. 'flow_duration': This measures the length of time of the flow and is essential for understanding the duration of connections, which can be an indicator of suspicious activities.
3. 'fwd_pkts_tot', 'bwd_pkts_tot': Total forward and backward packets give insights into the volume of data sent and received, which is crucial for detecting DoS attacks or data exfiltration attempts.
4. 'fwd_data_pkts_tot', 'bwd_data_pkts_tot': These columns indicate the total data packets in forward and backward directions, helping to understand data flows better and identify potential payload anomalies.
5. 'fwd_pkts_per_sec', 'bwd_pkts_per_sec', 'flow_pkts_per_sec': These metrics help measure the intensity of the traffic, crucial for identifying flooding attacks.
6. 'down_up_ratio': This ratio provides a quick insight into the symmetry of the communication flow, where significant imbalances might suggest command and control communications or data leakage.
7. 'fwd_header_size_tot', 'bwd_header_size_tot': The total size of packet headers sent in both directions can reveal attempts to exploit vulnerabilities through packet fragmentation.
8. 'flow_FIN_flag_count', 'flow_SYN_flag_count', 'flow_RST_flag_count': These flags are vital for understanding the state of the network connections and can indicate unusual terminations or requests that are common in scanning and denial-of-service attacks.
9. 'fwd_pkts_payload.max', 'fwd_pkts_payload.avg', 'fwd_pkts_payload.std', 'bwd_pkts_payload.max', 'bwd_pkts_payload.avg', 'bwd_pkts_payload.std': Payload statistics in both directions provide crucial insights into the distribution and variance of packet sizes, aiding in the detection of anomalies in data transfer.
10. 'fwd_iat.min', 'fwd_iat.max', 'bwd_iat.min', 'bwd_iat.max': These inter-arrival times help detect timed attacks or irregular traffic patterns.
11. 'payload_bytes_per_second': This measures the data flow rate, critical for identifying data exfiltration or flood attacks.
12. 'fwd_subflow_pkts', 'bwd_subflow_pkts': These columns help in understanding subflows within the main network flows, which can indicate multipartite attacks or fragmented traffic patterns.
13. 'active.min', 'active.max', 'active.std': Metrics on active times help detect long connections or periods of unusual activity, often associated with persistent threats.
14. 'fwd_last_window_size': Understanding the window size in the last packet of the forward direction can provide insights into the flow control mechanism and potential manipulation of the session.
15. 'traffic_category': This column categorizes traffic, allowing us to train our model more effectively by understanding the context of each network event.

These columns were specifically chosen because they offer the most direct insight into potentially malicious activities and anomalies in network traffic. By focusing on these metrics, we can build a more focused and effective machine learning model that is capable of detecting sophisticated cyber threats with higher accuracy. This streamlined dataset not only reduces computational load but also enhances the model’s ability to learn from the most impactful features.

## Results
The accuracy we got was 93% which consider as a good accuracy but the precision is low in cases of actual attack and this came from the data because the data contains only 2.4% attack cases and this didn't gave the model enough data of attack to have a better precision and this issue could be solved in the future by adding more datasets which increase precision. 


Discussion


Limitations:
1. The lack of available data online as an open source is an obsticale to improve the model efficiency.
2. 

Future Work:
We aim to incorporate real-time threat intelligence feeds and advanced algorithms to enhance the predictive accuracy and adaptability of our cybersecurity threat detection system.
