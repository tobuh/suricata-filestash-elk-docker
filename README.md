Suricata ELK with Filebeat-suricata-module
==========================================

This is a out-of-the-box approach of Suricata with ELK and Filebeat's suricata-module.

The advantage is: you get Dashboards directly with the Filebeat module.

# How to use

* Change your interface in docker-compose.xml
* Start with `docker-compose up -d`
* Navigate to http://your.ip.addr.ess:5601
* Look for "Dashboards" and search for "suricata". You will get the Dashboards
* Enjoy!

As this Docker image is used (https://github.com/jasonish/docker-suricata), you can use some additional commands:

* Update rules: `docker exec -it --user suricata suricata_suricata_1 suricata-update -f`
* Logrotate: `docker exec suricata_suricata_1 sudo logrotate /etc/logrotate.d/suricata`

# Further information

* https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-module-suricata.html
