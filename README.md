# MSPS
`msps` is the Mac Shell Proxy Setter. It takes care of all your shell proxy worries.

# Usage
`source msps <INTERFACE>` sets your `http_proxy`, `https_proxy` and `no_proxy` shell variables
according to the settings in your Mac Network preferences.

`<INTERFACE>` is the network interface name as given by `networksetup -listallnetworkservices`.

Put it into your `PATH` by downloading it with `curl -O https://raw.githubusercontent.com/noroute/msps/master/msps; chmod a+x msps`.

# Integration
Put `source msps "YOUR_FAVORITE_INTERFACE"` into the shell startup configuration file of your choice
(e.g. `.bashrc`, `.zshrc`). Remember that the configuration only takes place on shell startup and you have to `source` the script for the settings to have any effect on your actual shell.
Changes to your network settings in the preference pane will only become active for new shells
or when you re-source `msps`.
