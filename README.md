# Firewall-Setup-with-PfSense

<h2>Description</h2>
Project consists of a simple install of PfSense on an Unbuntu Server. 
<br />


<h2>Objectives</h2>


1. **Network Segmentation**:
    
    - **Objective**: <mark style="background: #BBFABBA6;">Create separate network segments (VLANs) for different devices or functions</mark> (e.g., IoT devices, workstations, and servers).
    - **Purpose**: Enhance security by isolating devices, reducing the risk of lateral movement in case of a breach.

2. **Firewall Configuration**:
    
    - **Objective**: <mark style="background: #BBFABBA6;">Implement and manage advanced firewall rules to control traffic between segments</mark>.
    - **Purpose**: Learn how to effectively block unwanted traffic and allow legitimate traffic based on security policies.

3. **Intrusion Detection and Prevention**:
    
    - **Objective**: <mark style="background: #BBFABBA6;">Set up packages like Snort or Suricata on pfSense to monitor and block suspicious activities.</mark>
    - **Purpose**: Gain experience in detecting and responding to security threats in real-time.

4. **Logging and Monitoring**:
    
    - **Objective**: <mark style="background: #BBFABBA6;">Use pfSense’s logging and monitoring tools to keep track of network activity and potential security incidents</mark>.
    - **Purpose**: Develop skills in analyzing logs and identifying signs of compromise or misuse.
  

**Network Interfaces**

<img width="883" height="880" alt="Screenshot 2025-09-20 203857" src="https://github.com/user-attachments/assets/ec4c8a6f-cb96-440a-9f0c-b31ddad72162" />

I'm adding 5 network adapters to correspond with the VMnet interfaces creating the segmentation of services and devices being added later.


<img width="719" height="457" alt="Screenshot 2025-09-20 210010" src="https://github.com/user-attachments/assets/c4439256-5d63-4bfd-a30c-d0f1da3d963f" />

- I now have IP address for WAN and LAN
- Selecting option 1, I can assign the interfaces and option 2 for IP addresses for the others



- In order to use the web configurator you need a web browser
- I installed an Unbuntu Desktop for this purpose


<img width="1365" height="802" alt="Screenshot 2025-09-20 225957" src="https://github.com/user-attachments/assets/503c893b-0c19-4662-ab2b-e857e5eca102" />



- I need to configure the interfaces with decription
- I will also setup interface opt3
  - this will be used as a span port
  - also known as port mirroring. Used to provide Security Onion with the network traffic it needs to perform its security monitoring and analysis functions
  - This provides it with a copy of the network traffic for inspection without disrupting a live network
  - also allows for the use of various tools like Suricata or Zeek to analyse packet data, forensic analysis
 

<img width="1196" height="707" alt="Screenshot 2025-09-20 230856" src="https://github.com/user-attachments/assets/91011267-182e-4cd1-a395-4f42d1994fe7" />




