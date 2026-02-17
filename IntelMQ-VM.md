
This is the Readme page for the **intelmq-vm** image that is pre-configured for Shadowserver feeds and includes IntelMQ, Elasticsearch, Logstash, and Kibana.

* https://interchange.shadowserver.org/image/ovf/v3.5.0/intelmq-vm-0.vmdk (3.1GB)
* https://interchange.shadowserver.org/image/ovf/v3.5.0/intelmq-vm.mf (66B)
* https://interchange.shadowserver.org/image/ovf/v3.5.0/intelmq-vm.ovf (15KB)

An API key is required and can be obtained by visiting https://www.shadowserver.org/contact/ and selecting _Report API Key Request_ under *What is this about?*.

This VM can be adapted to production use by removing the ShadowServerAPI-Collector `reports: test` setting and migrating the /opt/elasticsearch/data and /var/lib/postgresql directories to additional storage

 
# Details

## Versions

| | |
| --- | --- |
| Ubuntu | 24.04.3 LTS |
| IntelMQ | 3.5.0 |

## Ubuntu

The virtual machine is configured for DHCP.

| | |
| --- | --- |
| Login | `intelmq` |
| Password | `secret` |

## IntelMQ

| | |
| --- | --- |
| URL | http://{IP}/intelmq-manager/ |
| Login | `admin` |
| Password | `secret` |

## Fody

| | |
| --- | --- |
| URL | http://{IP}:8001 |
| Login | `fody` |
| Password | `secret` |

## Kibana

| | |
| --- | --- |
| URL | http://{IP}:5601/ |
| Login | `elastic` |
| Password | `*hMDPI-BQ6r4vNR*f*lC` |

# Process

1) Start the virtual machine

2) Login to intelmq-manager

3) Select **Configuration**

4) Select ShadowServerAPI-Collector and click _Edit Bot_

5) Set the api_key and secret.

6) Scroll to the bottom and click _OK_.

7) Click _Save Configuration_

8) Select **Management**

9) Under **Whole Botnet Status:** click Start

10) Login to Kibana

11) From the drop-down menu, select _Dashboards_ under **Analytics**

12) Click _Shadowserver Training Dashboard_

![image](images/dashboard.png)

