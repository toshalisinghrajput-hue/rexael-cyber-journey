# Module 3: Core SOC Solutions
## Room 4: Elastic Stack: The Basics
### What I learned about:
- ELK- ELK stands for Elasticsearch, Logstash, and Kibana. These are three open-source tools that are commonly used together to collect, store, analyse, and visualise data.  
ELK was originally developed to store, search, and visualize large amounts of data. Organizations used it to monitor application performance and perform searches on large datasets.  
Over time, its features made it popular in security operations as well. Now, many SOC teams use ELK almost as a SIEM solution.
- ELK's Core Components:
    - Elasticsearch: The first component, Elasticsearch, is a full-text search and analytics engine for JSON-formatted documents. It stores, analyzes, and correlates data and supports a RESTful API for interacting with it.
    -  Logstash: Logstash is a data processing engine that takes data from different sources, filters it, or normalizes it, and then sends it to the destination, which could be Kibana or a listening port.
    A Logstash configuration file is divided into three parts: Input, Output, and Filter.
    - Beats: Beats are host-based agents known as data-shippers that ship/transfer data from the endpoints to Elasticsearch. Each beat is a single-purpose agent that sends specific data to Elasticsearch.
    - Kibana: Kibana is a web-based data visualization tool that works with Elasticsearch to analyze, investigate, and visualize data streams in real time. It allows users to create multiple visualizations and dashboards for better visibility.
- How they Work Together:  
   - Beats collect data from multiple agents. For example, Winlogbeat collects Windows event logs, and Packetbeat collects network traffic flows.  
   - Logstash collects data from beats, ports, or files, parses/normalizes it into field value pairs, and stores them into Elasticsearch.  
   - Elasticsearch acts as a database used to search and analyze data.  
   - Kibana is responsible for displaying and visualizing the data stored in Elasticsearch. The data stored in Elasticsearch can easily be shaped into different visualizations, time charts, infographics, etc., using Kibana.
- 