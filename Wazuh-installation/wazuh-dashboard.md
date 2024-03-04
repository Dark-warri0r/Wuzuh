## Wazuh dashboard

To install and configure the Wazuh dashboard, you would execute the Wazuh installation assistant script with the `--wazuh-dashboard` option followed by the node name, and optionally, the port number for the dashboard. Here's how you can rewrite the command:

```bash
sudo bash wazuh-install.sh --wazuh-dashboard dashboard -p 8443
```

In this command:
- `sudo` is used to execute the command with elevated privileges.
- `bash wazuh-install.sh` invokes the Wazuh installation assistant script.
- `--wazuh-dashboard dashboard` specifies the installation of the Wazuh dashboard and assigns the node name as "dashboard".

---
#### optional  
As default it use port 443

- `-p 8443` specifies the port number (8443) on which the Wazuh dashboard will be accessible.

Make sure to replace `dashboard` with the actual node name used in your `config.yml` file for the initial configuration, if it differs. Also, ensure that you're running this command in the directory where the `wazuh-install.sh` script is located.
