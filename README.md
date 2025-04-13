# ELK-Stack

E-ELK- Elasticsearch is used to store logs such as Windows event logs sys logs, firewall logs.<br>
L-ELK- Logstash a pipeline line and collect the telemetry using elastic agents or beats.<br>
K-ELK- kibana is web console web GUI, visuailizations.<br>
## Diagram
![Screenshot 2024-10-03 200423](https://github.com/user-attachments/assets/40d71674-5017-4e21-a1cc-9323739ee140)<br>
## Steps
1. Elasticsearch setup<br>
-i m using a cloud provider VULTR it give 300$ cerdits,<br>
-sign up and create vpc and select location i have selected delhi<br>
-ipv4 set ip range 172.31.0.0/24 and give network name mydfir-soc-challenge<br>
-now create instance for elastic dedicated CPU,location delhi, ISO ubuntu 22.4 ,configuration 80gb 16 ram 4cpu disable ipv6 enable vpc and select our vpc name the instance mydfir-elk<br>
-create firewall rule ssh and my ip so that only we can access the ubuntu instance <br>
-open powerpoint and run ssh to connect to the instance we have created<br>
-update and upgrade using wget download elastic search conf deb x86<br>
-install elasticsearch using
```
dpkg -i <filename.deb>
```
-save the security autoconfiguration information in notepad<br>
-configure the elasticsearch.yml file 
```
nano /etc/elasticsearch/elasticsearch.yml
```
-remove # from host ip and port change to ubuntu instance ip and port 9200 save and exit<br>
-run this command so it will start the elasticsearch 
```
systemctl daemon-reload
systemctl enable elasticsearch.service
systemctl start elasticsearch.service
systemctl status elasticsearch.service
```
<br>

2.Kibana setup<br>
-copy the link address of kibana from browser conf deb x84 <br>
-download and install using wget and dpkg as shown above <br>
-change the .yml file at location
```
nano /etc/kibana/kibana.yml
```
-server port 5601 and ip of instance <br>
-and run the command 
```
systemctl daemon-reload
systemctl enable kibana.service
systemctl start kibana.service
systemctl status kibana.service
```
-now add another firewall rule tcp port 1-65535 and my ip so we can access in browser 
![Screenshot 2025-01-08 002054](https://github.com/user-attachments/assets/1ebadc54-96ff-4ea1-9e86-d4d98ba82b52)

![Screenshot 2025-01-08 002402](https://github.com/user-attachments/assets/2c24f26f-51f8-4d84-8355-9d68bedb96b9)

![Screenshot 2025-01-08 002402](https://github.com/user-attachments/assets/ac09282e-9623-49c4-aa29-1a45c183ad7c)

![Screenshot 2025-01-08 023702](https://github.com/user-attachments/assets/b1be10fe-9990-45c2-97c0-1b29a1c3a02a)
![Screenshot 2025-01-08 023717](https://github.com/user-attachments/assets/b9702739-caed-4b3b-9aee-28c5aa8a3544)
![Screenshot 2025-01-08 023733](https://github.com/user-attachments/assets/bad822e5-d4b4-4f03-bdb2-3de28e7a0291)
![Screenshot 2025-01-08 023801](https://github.com/user-attachments/assets/2ff30e36-db12-4ced-9b75-76ec38094fa1)
![Screenshot 2025-01-08 033207](https://github.com/user-attachments/assets/e1948c3a-d64b-4f11-92c1-d73f47ecde7a)

![Screenshot 2025-01-12 004134](https://github.com/user-attachments/assets/547edb0a-2ad7-464e-942a-25c284b91dbe)
![Screenshot 2025-01-12 010318](https://github.com/user-attachments/assets/1c1fd4c8-1e1a-418c-86cb-e145f55a590a)
