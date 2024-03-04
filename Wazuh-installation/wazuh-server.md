# Wazuh server
Run the following commands to install wazuh server


To run the Wazuh installation assistant with the `--wazuh-server` option followed by the node name to install the Wazuh server, you would typically execute a command similar to the following:

```bash
sudo bash wazuh-install.sh --wazuh-server wazuh-1
```

Replace ( `wazuh-1` = as default) with the actual node name used in your `config.yml` file for the initial configuration.

### our Wazuh server is now successfully installed.

---

If you want a Wazuh server single-node cluster, everything is set and you can proceed directly with Installing the Wazuh dashboard using the assisted installation method.

#### If you want a Wazuh server multi-node cluster, repeat this process on every Wazuh server node
