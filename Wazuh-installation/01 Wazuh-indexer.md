## Wazuh Installation

Follow these steps to install Wazuh Indexer

## Wazuh Indexer Installation

To download the Wazuh installation assistant (`wazuh-install.sh`) and the configuration file (`config.yml`), you can use the `curl` command as follows:

```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
curl -sO https://packages.wazuh.com/4.7/config.yml
```

These commands will download the Wazuh installation script and the configuration file into your current directory. After downloading, you can proceed with the installation and configuration of Wazuh.


Edit `config.yml` and replace the node names and IP values with the corresponding names and IP addresses `Then Run `

```bash

sudo bash wazuh-install.sh --generate-config-files

```
### Install and configure the Wazuh indexer nodes

Download the Wazuh installation assistant

```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh

```
Run the Wazuh installation assistant with the option --wazuh-indexer and the node name to install and configure the Wazuh indexer. The node name must be the same one used in config.yml for the initial configuration, for example, node-1 (default)

```bash
sudo bash wazuh-install.sh --wazuh-indexer node-1

```
## Cluster initialization

The final stage of installing the Wazuh indexer single-node or multi-node cluster consists of running the security admin script.

#### Run the Wazuh installation assistant with option --start-cluster on any Wazuh indexer node to load the new certificates information and start the cluster.

```bash
sudo bash wazuh-install.sh --start-cluster
```
---
## Testing the cluster installation
---
Run the following command to get the admin password.

```bash
sudo tar -axf wazuh-install-files.tar wazuh-install-files/wazuh-passwords.txt -O | grep -P "\'admin\'" -A 1
```

Run the following command to confirm that the installation is successful. Replace <ADMIN_PASSWORD> with the password gotten from the output of the previous command. Replace <WAZUH_INDEXER_IP> with the configured Wazuh indexer IP address

```bash
curl -k -u admin:<ADMIN_PASSWORD> https://<WAZUH_INDEXER_IP>:9200

```

Run the following command to check if the cluster is working correctly.

```bash
curl -k -u admin:<ADMIN_PASSWORD> https://<WAZUH_INDEXER_IP>:9200/_cat/nodes?v
```
---
#### The Wazuh indexer is now successfully installed, and you can proceed with installing the Wazuh server.

---
Next install Server
