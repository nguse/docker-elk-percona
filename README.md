# ELK/Percona Log Parsing Stack

This repo is a fork from: https://github.com/deviantony/docker-elk  

# Purpose

Logstash configuration has been modified such that it will ingest the Percona General log format and do some helpful things.  

# Notes:

Configuration required!  

You will need to edit the docker-compose.yml file to adjust the volume mounted to the logstash container.  
`- /foobar/logs:/logs:ro`

You may also need to edit the logstash configuration (logstash/config/logstash.conf) to control what it ingests.  
`path => "/logs/general-*.log"`
