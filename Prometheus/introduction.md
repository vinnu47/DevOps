Prometheus is an open-source monitoring tool that collects metrics data, and provide tools to visualize the collected data  

In addition, promotheus allows you to generate alerts when metrics reach a user specified threshold  

Prometheus collects metrics by scraping tarfets who expose metrics through an HTTP endpoint 


Metrics used for Prometheus Monitor
- CPU/Memory Utlization
- Disk Space
- Service Uptime
- Application specific data
  - Number of exceptions
  - latency
  - Pending Requests  

Prometheus is designed to monitor time-series data that is numeric   

what type data should prometheus not monitor
- Events
- System logs
- Traces

![alt text](./Images/image24.png)  

client libraries  
monitor application metrics  
- Number of errors/exceptions
- Latenct of requests
- job execution time

Prometheus comes with client libraries that allow you to expose any application metrics you need prometheus to track

language support:
- Go
- Java
- Python
- Ruby
- Rust

Pull based mode  
Prometheus needs to have a list of all targets it should scrape. other solutions include zabix, nagios.  
In a pushed based model, the targets are configured to push the metric data to the metrics server. other solutions include Logstash, Graphite, OpenTSDB   

Why pull?   
some of the benefits include   
- Easier to tell if a target is down    
  - In a pushed based system we dont know if its down or has been decommissioned  
- push based systems could potentially overload metrics server if too many incoming connections get flooded at same time.   
- pull based system have a definitive list of targets to monitor, creating a central source of truth   

why push?
- event-based systems, pulling data wouldnt be a viable option
  - however, prometheus is for collecting metrics and not monitoring events.
- short lived jobs, as they may end before a pull can occur
  - prometheus has feature called pushgateway to handle this situation.
  