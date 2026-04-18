# Beats

> Data collector & shippers

## What are Beats?

Beats are lightweight agents that collect data from systems and send it into the Elastic stack.

Common examples:

- `Filebeat`: ships log files
- `Metricbeat`: ships system and service metrics
- `Packetbeat`: captures network traffic metadata
- `Auditbeat`: ships audit/security data
- `Heartbeat`: checks service uptime

In many setups, Beats send data to Logstash for parsing and enrichment, though they can also send data directly to Elasticsearch.

## Where are Beats run?

They are installed and run as another service on systemd that runs on **each** of the machines.

## What is a Harvester?

Within Filebeat, there are Harvesters.
Harvesters monitor a file on the disk and listen for changes.
They create new events for each new line it reads, then streams them.
