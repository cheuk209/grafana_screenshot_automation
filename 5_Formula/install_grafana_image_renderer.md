We need to install grafana image renderer.

Sure, I can help with that! To install Grafana CLI in your CodeSpace terminal, follow these steps:

1. **Open your terminal** in CodeSpace.
2. **Install Grafana CLI** using the following command:

   ```bash
   npm install -g @grafana/cli
   ```

3. **Verify the installation** by checking the version of Grafana CLI:

   ```bash
   grafana-cli --version
   ```

This should install the Grafana CLI globally on your system, making it available for use in any project.

Let me know if you encounter any issues or need further assistance!


kubectl get pods -n grafana-monitoring

kubectl exec -it grafana-abc1234-xyz5678 -n grafana-monitoring -- /bin/bash


 kubectl exec -it grafana-5949bd8786-rlt89 -n grafana-monitoring -- /bin/bash
I have no name!@grafana-5949bd8786-rlt89:/opt/bitnami/grafana$ grafana cli
NAME:
   grafana cli - run the grafana cli

USAGE:
   grafana cli command [command options] 

COMMANDS:
   plugins  Manage plugins for grafana
   admin    Grafana admin commands
   help, h  Shows a list of commands or help for one command

OPTIONS:
   --config value           Path to config file
   --homepath value         Path to Grafana install/home path, defaults to working directory
   --configOverrides value  Configuration options to override defaults as a string. e.g. cfg:default.paths.log=/dev/null
   --version, -v            print the version
   --debug                  Enable debug logging (default: false)
   --pluginsDir value       Path to the Grafana plugin directory (default: "/var/lib/grafana/plugins") [$GF_PLUGIN_DIR]
   --repo value             URL to the plugin repository (default: "https://grafana.com/api/plugins") [$GF_PLUGIN_REPO]
   --pluginUrl value        Full url to the plugin zip file instead of downloading the plugin from grafana.com/api [$GF_PLUGIN_URL]
   --insecure               Skip TLS verification (insecure) (default: false)
   --help, -h               show help
I have no name!@grafana-5949bd8786-rlt89:/opt/bitnami/grafana$ 

grafana-cli plugins install grafana-image-renderer
