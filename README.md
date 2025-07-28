# Real-Time-Network-Anomaly-Detection
Real-time network anomaly detection leveraging live packet capture, intrusion detection systems, and machine learning.

  Project Overview
This project presents a modular, dockerized pipeline for real-time network anomaly detection leveraging live packet capture, intrusion detection systems, and machine learning.
The system operates as follows:

  Live Packet Capture:
Network packets are captured in real time using tools like tcpdump, tshark, or scapy. Captured traffic is periodically saved into .pcap files (e.g., every 5 minutes) through an automated script or cron job.

  Traffic Enrichment with IDS:
Each .pcap file is processed by powerful IDS tools such as Zeek, Suricata, or Snort. These tools extract detailed logs (e.g., HTTP, DNS, SSL, alerts), providing enriched insights into network behavior and potential threats.

  Machine Learning-Based Anomaly Detection:
Extracted logs and features—such as connection durations, byte counts, protocols, signatures, and network flow statistics—are fed into unsupervised anomaly detection algorithms (e.g., Isolation Forest, Autoencoders, LSTM-based models) implemented with frameworks such as scikit-learn, TensorFlow, or PyTorch.

  Automated and Near Real-Time Analysis:
The system continuously analyzes enriched network data, flags suspicious activity, and can notify users or security systems, enabling timely response to emerging anomalies.

  Dockerized Deployment:
The entire pipeline is containerized with Docker to simplify deployment, scalability, and environment consistency. This enables you to easily run the system across different machines or cloud environments without complex setup.

This flexible and portable architecture supports advanced network monitoring, rapid detection of novel threats, and straightforward integration into SOC workflows or research environments.

Explore the repository to deploy a ready-to-use, end-to-end anomaly detection platform for your network traffic data — all easily managed via Docker.
