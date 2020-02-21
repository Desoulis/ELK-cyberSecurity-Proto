# ELK-cyberSecurity-Proto
Idea of prototype is piping windows logs from WinLogBeat (deployed locally) => Logstash (deployed on EC2) => AWS ElasticSearch/Kibana => Elastalert.

Elastalert contains security rules generated from Sigma which analyzes logs, and generates security alert (which could in turn be pipelined to slack ala "Detects suspicious PowerShell download command" under elastalert/rules/sigma_powershell)

Project contains config files enabling pipelining and some of the rules, for installation of each individual service, see:

WinLogBeat: https://www.youtube.com/watch?v=grloDtOS21c

Logstash: https://aws.amazon.com/elasticsearch-service/resources/articles/logstash-tutorial/

Elastalert: https://elastalert.readthedocs.io/en/latest/running_elastalert.html

This is a work in progress and the rules on elastalert side is not working in generating alerts as intended.
