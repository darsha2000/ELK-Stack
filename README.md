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


