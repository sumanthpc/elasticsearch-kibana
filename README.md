# elasticsearch-kibana
Elastic Search Kibana

### Fork the repo / Create devcontainer config.

The path `.devcontainer/config/devcontainer.json` contains the following configuration.

```json
{
  "image": "mcr.microsoft.com/devcontainers/universal:2",
  "features": {
    "ghcr.io/devcontainers-contrib/features/elasticsearch-asdf:2": {}
  }
}
```

Create Codespace on Config with 4GB Machine.
After codepsace has initialized with elastic search follow the steps.

### Download Kibana 

Download deb version at https://www.elastic.co/downloads/kibana
Current version is https://artifacts.elastic.co/downloads/kibana/kibana-8.10.3-amd64.deb

### ElasticSearch

```bash
elasticsearch
```
 Copy the keys at the end of the logs.

 ### Verify Elastic Search

 ```bash
curl https://localhost:9200 -u "elastic:PASS" -k
 ```

### Install and run Kibana

Install Kibana DEB Package.
```bash
sudo apt install ./kibana-8.10.3-amd64.deb
```

Create Empty Kibana Config File.
```bash
touch kibana_conf.yml
```

Run Kibana
```bash
sudo /usr/share/kibana/bin/kibana -c kibana_conf.yml --allow-root
```

### Register Kibana

1. Enter Enrollment Key under Elastic Search Log
2. Enter Verification code under Kibana Log
3. Login and use Kibana


## Note

This is not a standard way to install ELK Stack.
This is just for creating temporary Elastic + Kibana setup for learning.
