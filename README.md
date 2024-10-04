# ELK-Stack

E-ELK- Elasticsearch is used to store logs such as Windows event logs sys logs, firewall logs.<br>
L-ELK- Logstash a pipeline line and collect the telemetry using elastic agents or beats.<br>
K-ELK- kibana is web console web GUI, visuailizations.<br>
## Diagram
![Screenshot 2024-10-03 200423](https://github.com/user-attachments/assets/40d71674-5017-4e21-a1cc-9323739ee140)<br>
## Steps
1. Elasticsearch setup<br>
i m using a cloud provider VULTR it give 300$ cerdits,
sign up and create vpc and select location i have selected delhi
ipv4 set ip range 172.31.0.0/24 and give network name mydfir-soc-challenge
now create instance for elastic dedicated CPU,location delhi, ISO ubuntu 22.4 ,configuration 80gb 16 ram 4cpu disable ipv6 enable vpc and select our vpc name the instance mydfir-elk
open powerpoint and run ssh to connect to the instance we have created
update and upgrade using wget download elastci searh conf deb x86
install elasticsearch using
```
dpkg -i <filename.deb>
```
save the security autoconfiguration information in notepad





