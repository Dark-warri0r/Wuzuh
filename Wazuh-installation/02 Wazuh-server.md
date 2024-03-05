## Wazuh server



Run the Wazuh installation assistant with the option `--wazuh-server` followed by the node name to install the Wazuh server. The node name must be the same one used in `config.yml` for the initial configuration, for example, `wazuh-1`

```bash
sudo bash wazuh-install.sh --wazuh-server wazuh-1
```


### Our Wazuh server is now successfully installed.

If you want a Wazuh server single-node cluster, everything is set and you can proceed directly with Installing the Wazuh dashboard using the assisted installation method.

If you want a Wazuh server multi-node cluster, repeat this process on every Wazuh server node

---

### Next install the Wazuh dashboard
